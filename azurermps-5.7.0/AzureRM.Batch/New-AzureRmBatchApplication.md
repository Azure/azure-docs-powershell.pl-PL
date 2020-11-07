---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718655"
---
# <span data-ttu-id="86b21-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="86b21-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="86b21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86b21-102">SYNOPSIS</span></span>
<span data-ttu-id="86b21-103">Dodaje aplikację do określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="86b21-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86b21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86b21-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86b21-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86b21-105">DESCRIPTION</span></span>
<span data-ttu-id="86b21-106">Polecenie cmdlet **New-AzureRmBatchApplication** umożliwia dodanie aplikacji do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="86b21-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="86b21-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86b21-107">EXAMPLES</span></span>

### <span data-ttu-id="86b21-108">Przykład 1: Dodawanie pustej aplikacji do konta partii</span><span class="sxs-lookup"><span data-stu-id="86b21-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="86b21-109">To polecenie tworzy aplikację Przykładowa na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="86b21-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="86b21-110">Aplikacja początkowo nie zawiera żadnych pakietów.</span><span class="sxs-lookup"><span data-stu-id="86b21-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="86b21-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86b21-111">PARAMETERS</span></span>

### <span data-ttu-id="86b21-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86b21-112">-AccountName</span></span>
<span data-ttu-id="86b21-113">Określa nazwę konta wsadowego, do którego jest dodawana aplikacja.</span><span class="sxs-lookup"><span data-stu-id="86b21-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="86b21-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="86b21-114">-AllowUpdates</span></span>
<span data-ttu-id="86b21-115">Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="86b21-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b21-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="86b21-116">-ApplicationId</span></span>
<span data-ttu-id="86b21-117">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86b21-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="86b21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b21-118">-DefaultProfile</span></span>
<span data-ttu-id="86b21-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86b21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86b21-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86b21-120">-DisplayName</span></span>
<span data-ttu-id="86b21-121">Określa nazwę wyświetlaną dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86b21-121">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b21-122">-ResourceGroupName</span></span>
<span data-ttu-id="86b21-123">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="86b21-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="86b21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b21-124">CommonParameters</span></span>
<span data-ttu-id="86b21-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b21-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b21-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b21-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86b21-127">INPUTS</span></span>

### <span data-ttu-id="86b21-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="86b21-128">None</span></span>
<span data-ttu-id="86b21-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="86b21-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86b21-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86b21-130">OUTPUTS</span></span>

### <span data-ttu-id="86b21-131">Microsoft.Azure.Commands.Batch. Modele. PSApplication</span><span class="sxs-lookup"><span data-stu-id="86b21-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="86b21-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86b21-132">NOTES</span></span>

## <span data-ttu-id="86b21-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86b21-133">RELATED LINKS</span></span>

[<span data-ttu-id="86b21-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="86b21-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="86b21-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="86b21-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="86b21-136">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="86b21-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="86b21-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="86b21-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="86b21-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="86b21-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="86b21-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="86b21-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


