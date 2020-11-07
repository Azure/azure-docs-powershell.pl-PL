---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890122"
---
# Add-AzVMAdditionalUnattendContent

## STRESZCZENIe
Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.

## POLECENIA

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVMAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.
Określ dodatkowe kodowanie Base 64 informacje o formacie XML, które to polecenie cmdlet dodaje do pliku unattend.xml.

## Przykłady

### Przykład 1: dodawanie zawartości do unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.

Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.

Trzecie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.
Polecenie monituje o podanie nazwy użytkownika i hasła.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .

W czwartym poleceniu użyto polecenia cmdlet **Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.

W piątym poleceniu jest przypisywana zawartość zmiennej $AucContent.
Zawartość zawiera hasło.

Polecenie ostatnie powoduje dodanie zawartości przechowywanej w $AucContent do pliku unattend.xml.

## PARAMETRÓW

### -Content (zawartość)
Określa zakodowaną w podstawie 64 zawartość w formacie XML.
To polecenie cmdlet umożliwia dodanie zawartości do pliku unattend.xml.
Zawartość XML musi być mniejsza niż 4 KB i musi zawierać element główny ustawienia lub funkcję, które zostaną wstawione przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingName
Określa nazwę ustawienia, którego dotyczy zawartość.
Dopuszczalne wartości tego parametru to:

- FirstLogonCommands
- Autologowanie

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .
Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSVirtualMachine
Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Nowe — AzVMConfig](./New-AzVMConfig.md)
