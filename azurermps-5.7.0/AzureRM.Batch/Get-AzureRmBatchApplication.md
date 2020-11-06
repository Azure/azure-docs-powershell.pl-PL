---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525349"
---
# <span data-ttu-id="909a2-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="909a2-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="909a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="909a2-102">SYNOPSIS</span></span>
<span data-ttu-id="909a2-103">Pobiera informacje o określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="909a2-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="909a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="909a2-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="909a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="909a2-105">DESCRIPTION</span></span>
<span data-ttu-id="909a2-106">Polecenie cmdlet **Get-AzureRmBatchApplication** pobiera informacje o aplikacji z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="909a2-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="909a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="909a2-107">EXAMPLES</span></span>

### <span data-ttu-id="909a2-108">Przykład 1. Wyświetlanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="909a2-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="909a2-109">To polecenie wyświetla wszystkie aplikacje na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="909a2-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="909a2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="909a2-110">PARAMETERS</span></span>

### <span data-ttu-id="909a2-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="909a2-111">-AccountName</span></span>
<span data-ttu-id="909a2-112">Określa nazwę konta wsadowego zawierającego odpowiednią aplikację.</span><span class="sxs-lookup"><span data-stu-id="909a2-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="909a2-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="909a2-113">-ApplicationId</span></span>
<span data-ttu-id="909a2-114">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="909a2-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="909a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909a2-115">-DefaultProfile</span></span>
<span data-ttu-id="909a2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="909a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="909a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="909a2-118">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="909a2-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="909a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909a2-119">CommonParameters</span></span>
<span data-ttu-id="909a2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909a2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="909a2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909a2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="909a2-122">INPUTS</span></span>

### <span data-ttu-id="909a2-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="909a2-123">None</span></span>
<span data-ttu-id="909a2-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="909a2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="909a2-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="909a2-125">OUTPUTS</span></span>

### <span data-ttu-id="909a2-126">Microsoft.Azure.Commands.Batch. Modele. PSApplication</span><span class="sxs-lookup"><span data-stu-id="909a2-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="909a2-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="909a2-127">NOTES</span></span>

## <span data-ttu-id="909a2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="909a2-128">RELATED LINKS</span></span>

[<span data-ttu-id="909a2-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="909a2-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="909a2-130">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="909a2-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="909a2-131">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="909a2-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="909a2-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="909a2-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="909a2-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="909a2-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="909a2-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="909a2-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


