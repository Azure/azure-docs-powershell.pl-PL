---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
ms.openlocfilehash: c8109a1fa13bff2a2a527bb7e1f9cb232d0e61c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899002"
---
# Add-AzureRmVMSshPublicKey

## STRESZCZENIe
Dodaje klucze publiczne dla protokołu SSH dla maszyny wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureRmVMSshPublicKey** umożliwia dodanie kluczy publicznych, których można używać do nawiązywania połączenia z maszyną wirtualną za pośrednictwem bezpiecznego powłoki (SSH).

## Przykłady

### Przykład 1: Dodawanie klucza publicznego do maszyny wirtualnej
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .
Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.

Drugie polecenie dodaje klucz publiczny do lokalizacji na VirtualMachine07, że parametr path określa.

## PARAMETRÓW

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

### -Dane
Określa kodowanie bazowe 64 klucza publicznego.
Możesz połączyć się z maszyną wirtualną przy użyciu protokołu SSH lub przy użyciu klucza określającego ten parametr.

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

### -Path
Określa pełną ścieżkę pliku na maszynie wirtualnej, gdzie to polecenie cmdlet przechowuje klucz publiczny SSH.
Jeśli plik już istnieje, to polecenie cmdlet dołącza klucz do pliku.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .
Za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) można utworzyć obiekt maszyny wirtualnej.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSVirtualMachine
Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Nowe — AzureRmVMConfig](./New-AzureRmVMConfig.md)
