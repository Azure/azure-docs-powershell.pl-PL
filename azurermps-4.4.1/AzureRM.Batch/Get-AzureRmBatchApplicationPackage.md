---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546284"
---
# <span data-ttu-id="94c37-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="94c37-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="94c37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94c37-102">SYNOPSIS</span></span>
<span data-ttu-id="94c37-103">Pobiera informacje o pakiecie aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="94c37-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94c37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94c37-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94c37-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94c37-105">DESCRIPTION</span></span>
<span data-ttu-id="94c37-106">Polecenie cmdlet **Get-AzureRmBatchApplicationPackage** pobiera informacje o pakiecie aplikacji na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="94c37-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="94c37-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94c37-107">EXAMPLES</span></span>

### <span data-ttu-id="94c37-108">Przykład 1: uzyskiwanie szczegółowych informacji o pakiecie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="94c37-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="94c37-109">To polecenie pobiera szczegóły wersji 1,0 pakietu przykładowa.</span><span class="sxs-lookup"><span data-stu-id="94c37-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="94c37-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94c37-110">PARAMETERS</span></span>

### <span data-ttu-id="94c37-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94c37-111">-AccountName</span></span>
<span data-ttu-id="94c37-112">Określa nazwę konta wsadowego, z którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="94c37-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c37-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="94c37-113">-ApplicationId</span></span>
<span data-ttu-id="94c37-114">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="94c37-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c37-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="94c37-115">-ApplicationVersion</span></span>
<span data-ttu-id="94c37-116">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="94c37-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c37-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c37-117">-ResourceGroupName</span></span>
<span data-ttu-id="94c37-118">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="94c37-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c37-119">-DefaultProfile</span></span>
<span data-ttu-id="94c37-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94c37-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c37-121">CommonParameters</span></span>
<span data-ttu-id="94c37-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c37-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c37-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c37-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94c37-124">INPUTS</span></span>

## <span data-ttu-id="94c37-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94c37-125">OUTPUTS</span></span>

### <span data-ttu-id="94c37-126">Microsoft.Azure.Commands.Batch. Modele. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="94c37-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="94c37-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94c37-127">NOTES</span></span>

## <span data-ttu-id="94c37-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94c37-128">RELATED LINKS</span></span>

[<span data-ttu-id="94c37-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="94c37-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="94c37-130">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="94c37-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="94c37-131">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="94c37-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="94c37-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="94c37-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="94c37-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="94c37-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="94c37-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="94c37-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


