---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527597"
---
# Get-AzureRmDataLakeStoreAccount

## STRESZCZENIe
Pobiera szczegóły konta usługi Data Lake Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Wszystkie w abonamentach (domyślnie)
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Cała grupa zasobów
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Określone konto
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDataLakeStoreAccount** pobiera szczegóły konta usługi Data Lake Store.

## Przykłady

### Przykład 1: Uzyskiwanie konta w usłudze Data Lake Store
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

To polecenie uzyskuje konto o nazwie ContosoADL.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę konta, które ma zostać pozyskane.

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store, które ma zostać nadane.

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSDataLakeStoreAccount
Twoje konto usługi Data Lake Store z prośbą o szczegółowe dane.

### Lista<PSDataLakeStoreAccount>
Lista kont usługi Data Lake Store w określonej grupie zasobów lub subskrypcji.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[Remove-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[Set-AzureRmDataLakeStoreAccount](./Set-AzureRmDataLakeStoreAccount.md)

[Test — AzureRmDataLakeStoreAccount](./Test-AzureRmDataLakeStoreAccount.md)


