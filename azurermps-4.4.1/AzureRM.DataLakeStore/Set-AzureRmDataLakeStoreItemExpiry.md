---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554372"
---
# <span data-ttu-id="a8bf9-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a8bf9-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="a8bf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bf9-103">Ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8bf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8bf9-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8bf9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bf9-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemExpiry** ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="a8bf9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="a8bf9-108">Przykład 1. Ustawianie czasu wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="a8bf9-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="a8bf9-109">Umożliwia ustawienie daty wygaśnięcia dla pliku myfile.txt na koncie ContosoADL od razu do dwóch godzin.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="a8bf9-110">Spowoduje to wygaśnięcie pliku (oznaczenie go do usunięcia) w ciągu dwóch godzin.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="a8bf9-111">Przykład 2: usuwanie wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="a8bf9-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="a8bf9-112">Usuwa wszystkie wygaśnięcia, które zostały wcześniej ustawione w pliku "myfile.txt" na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="a8bf9-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="a8bf9-113">Oznacza to, że plik nie zostanie automatycznie wygaśnie (oznaczony do usunięcia) i trzeba będzie ręcznie usunąć lub ponownie ustawić ważność.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="a8bf9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8bf9-114">PARAMETERS</span></span>

### <span data-ttu-id="a8bf9-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="a8bf9-115">-Account</span></span>
<span data-ttu-id="a8bf9-116">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-116">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bf9-117">-Data wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="a8bf9-117">-Expiration</span></span>
<span data-ttu-id="a8bf9-118">Bezwzględny czas wygaśnięcia określonego pliku.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="a8bf9-119">Jeśli nie ma wartości ani nie jest ustawiona wartość MaxValue, plik nigdy nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bf9-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a8bf9-120">-Path</span></span>
<span data-ttu-id="a8bf9-121">Określa ścieżkę do usługi Data Lake Store dla elementu pliku, dla którego ma zostać ustawiony lub usunięty wygasanie.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bf9-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8bf9-122">-Confirm</span></span>
<span data-ttu-id="a8bf9-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8bf9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bf9-124">-WhatIf</span></span>
<span data-ttu-id="a8bf9-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bf9-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8bf9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bf9-127">-DefaultProfile</span></span>
<span data-ttu-id="a8bf9-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8bf9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bf9-129">CommonParameters</span></span>
<span data-ttu-id="a8bf9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bf9-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bf9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bf9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8bf9-132">INPUTS</span></span>

## <span data-ttu-id="a8bf9-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8bf9-133">OUTPUTS</span></span>

### <span data-ttu-id="a8bf9-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a8bf9-134">DataLakeStoreItem</span></span>
<span data-ttu-id="a8bf9-135">Zaktualizowany plik o nowym czasie wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="a8bf9-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="a8bf9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8bf9-136">NOTES</span></span>
<span data-ttu-id="a8bf9-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a8bf9-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="a8bf9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8bf9-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8bf9-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a8bf9-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

