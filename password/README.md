<table>
 <tr>
  <th>Password</th>
  <th>Password Revealed</th>
 </tr>
 <tr>
  <td>
    <img width="600" alt="image" src="password.svg">
  </td>
  <td>
    <img width="600" alt="image" src="password_revealed.svg">
  </td>
 </tr>
</table>

Copy React Component to your project:

```tsx
import React, { memo, SVGProps } from "react";

interface PasswordIconProps extends SVGProps<SVGSVGElement> {
	show?: boolean;
	width?: number;
	height?: number;
}
const PasswordIcon: React.FC<PasswordIconProps> = ({ show, width, height, ...props }: PasswordIconProps) => {
	if (show) {
		return (
			<svg
				version="1.1"
				focusable="false"
				xmlns="http://www.w3.org/2000/svg"
				xmlnsXlink="http://www.w3.org/1999/xlink"
				x="0px"
				y="0px"
				viewBox="0 0 10.8 9"
				fill="currentColor"
				xmlSpace="preserve">
				<pathd="M5.4,0c2.7,0,4.9,1.9,5.4,4.5C10.3,7.1,8.1,9,5.4,9S0.5,7.1,0,4.5C0.5,1.9,2.7,0,5.4,0z M5.4,8c2.1,0,3.9-1.5,4.4-3.5
	c-0.6-2.4-3-3.9-5.4-3.4C2.7,1.5,1.4,2.8,1,4.5C1.5,6.5,3.3,8,5.4,8z M5.4,6.8c-1.2,0-2.2-1-2.2-2.2s1-2.2,2.2-2.2s2.2,1,2.2,2.2
	S6.7,6.8,5.4,6.8L5.4,6.8z M5.4,5.8c0.7,0,1.2-0.6,1.2-1.2S6.1,3.2,5.4,3.2S4.2,3.8,4.2,4.5S4.7,5.8,5.4,5.8z"
				/>
			</svg>
		);
	}
	return (
		<svg
			version="1.1"
			focusable="false"
			xmlns="http://www.w3.org/2000/svg"
			xmlnsXlink="http://www.w3.org/1999/xlink"
			x="0px"
			y="0px"
			viewBox="0 0 10.8 6.1"
			fill="currentColor"
			xmlSpace="preserve">
			<path
				d="M4.1,6.1l-1-0.3l0.4-1.5C2.9,4.1,2.4,3.8,1.9,3.4L0.8,4.5L0.1,3.8l1.1-1.1C0.6,2,0.2,1.1,0,0.2L1,0c0.4,2.1,2.2,3.7,4.4,3.7
	c2.2,0,4-1.6,4.4-3.7l1,0.2C10.7,1.1,10.2,2,9.6,2.7l1.1,1.1L10,4.5L8.9,3.4c-0.5,0.4-1,0.7-1.6,0.9l0.4,1.5l-1,0.3L6.3,4.6
	c-0.6,0.1-1.3,0.1-1.9,0C4.5,4.6,4.1,6.1,4.1,6.1z"
			/>
		</svg>
	);
};

PasswordIcon.defaultProps = {
	show: false,
	width: 24,
	height: 24,
};
export default memo(PasswordIcon);
```
