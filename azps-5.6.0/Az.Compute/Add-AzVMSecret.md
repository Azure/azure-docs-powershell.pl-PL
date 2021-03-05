---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962465"
---
# Add-AzVMSecret

## SYNOPSIS
Dodaje klucz tajny do maszyny wirtualnej.

## SKŁADNIA

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVMSecret** dodaje klucz tajny do maszyny wirtualnej.
Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.
Klucz tajny musi być przechowywany w magazynie kluczy.
Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [Co to jest magazyn kluczy platformy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
Aby uzyskać więcej informacji o poleceniach cmdlet, zobacz polecenia [cmdlet](/powershell/module/az.keyvault) magazynu kluczy platformy Azure lub polecenie cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## PRZYKŁADY

### Przykład 1. Dodawanie tajemnicy do maszyny wirtualnej
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Drugie polecenie tworzy obiekt poświadczeń przy użyciu Get-Credential cmdlet, a następnie zapisuje wynik w $Credential danych.
Polecenie monituje o nazwę użytkownika i hasło.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .
Trzecie polecenie używa **polecenia cmdlet Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.
Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId do późniejszego użycia.
W tym poleceniu założono, że $SubscriptionId zmienna ma odpowiednią wartość.
Piąte polecenie przypisuje wartość do zmiennej $CertificateStore 01 do późniejszego użycia.
Szóste polecenie przypisuje adres URL magazynu certyfikatów.
Siódme polecenie dodaje klucz tajny do maszyny wirtualnej przechowywanej w $VirtualMachine.
Parametr SourceVaultId określa magazyn kluczy.
To polecenie określa nazwę magazynu certyfikatów i adres URL certyfikatu.
Dodatek **AzVMSecret można wielokrotnie uruchamiać** w celu dodania sekretów innych certyfikatów.

## PARAMETERS

### -CertificateStore
Określa nazwę magazynu certyfikatów na maszyny wirtualnej, na których działa system operacyjny Windows.
To polecenie cmdlet dodaje certyfikat do magazynu, który określa ten parametr.
Ten parametr można określić tylko dla maszyn wirtualnych, na których działa system operacyjny Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Określa adres URL, który wskazuje klucz tajny magazynu kluczy, który zawiera certyfikat.
Certyfikat jest kodowaniem Base64 następującego obiektu JavaScript Object Notation (JSON), który jest kodowany w formacie UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", ""password": " } Obecnie typ_danych akceptuje tylko pliki \<pfx-file-password\> pfx.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Określa identyfikator zasobu magazynu kluczy zawierający certyfikaty, które można dodać do maszyny wirtualnej.
Ta wartość działa również jako klucz do dodawania wielu certyfikatów.
Oznacza to, że można użyć tej samej wartości dla wartości *SourceVaultId* podczas dodawania wielu certyfikatów z tego samego magazynu kluczy.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — MASZYNY WIRTUALNEJ
Określa obiekt maszyny wirtualnej, który zostanie zmodyfikowany przez to polecenie cmdlet.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)
Aby utworzyć obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
