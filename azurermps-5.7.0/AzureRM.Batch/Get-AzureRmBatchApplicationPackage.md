---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 609c7e161b131d80f9b41355f13ced8636a591e8
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554406"
---
# <span data-ttu-id="1961d-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1961d-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="1961d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1961d-102">SYNOPSIS</span></span>
<span data-ttu-id="1961d-103">Pobiera informacje o pakiecie aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="1961d-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1961d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1961d-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1961d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1961d-105">DESCRIPTION</span></span>
<span data-ttu-id="1961d-106">Polecenie cmdlet **Get-AzureRmBatchApplicationPackage** pobiera informacje o pakiecie aplikacji na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="1961d-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="1961d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1961d-107">EXAMPLES</span></span>

### <span data-ttu-id="1961d-108">Przykład 1: uzyskiwanie szczegółowych informacji o pakiecie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="1961d-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="1961d-109">To polecenie pobiera szczegóły wersji 1,0 pakietu przykładowa.</span><span class="sxs-lookup"><span data-stu-id="1961d-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="1961d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1961d-110">PARAMETERS</span></span>

### <span data-ttu-id="1961d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1961d-111">-AccountName</span></span>
<span data-ttu-id="1961d-112">Określa nazwę konta wsadowego, z którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="1961d-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1961d-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="1961d-113">-ApplicationId</span></span>
<span data-ttu-id="1961d-114">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1961d-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1961d-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="1961d-115">-ApplicationVersion</span></span>
<span data-ttu-id="1961d-116">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1961d-116">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1961d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1961d-117">-DefaultProfile</span></span>
<span data-ttu-id="1961d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1961d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1961d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1961d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1961d-120">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="1961d-120">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1961d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1961d-121">CommonParameters</span></span>
<span data-ttu-id="1961d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1961d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1961d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1961d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1961d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1961d-124">INPUTS</span></span>

### <span data-ttu-id="1961d-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1961d-125">None</span></span>
<span data-ttu-id="1961d-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1961d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1961d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1961d-127">OUTPUTS</span></span>

### <span data-ttu-id="1961d-128">Microsoft.Azure.Commands.Batch. Modele. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1961d-128">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="1961d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1961d-129">NOTES</span></span>

## <span data-ttu-id="1961d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1961d-130">RELATED LINKS</span></span>

[<span data-ttu-id="1961d-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1961d-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="1961d-132">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1961d-132">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="1961d-133">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1961d-133">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1961d-134">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1961d-134">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="1961d-135">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1961d-135">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1961d-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1961d-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


