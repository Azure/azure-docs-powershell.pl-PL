---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: df7229668547e1c018067effe50e823354d64736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553688"
---
# <span data-ttu-id="a24b9-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a24b9-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a24b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a24b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a24b9-103">Usuwa aplikację z konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a24b9-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a24b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a24b9-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a24b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a24b9-106">Polecenie cmdlet **Remove-AzureRmBatchApplication** usuwa aplikację z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="a24b9-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="a24b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a24b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a24b9-108">Przykład 1: Usuwanie aplikacji z konta partii</span><span class="sxs-lookup"><span data-stu-id="a24b9-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="a24b9-109">To polecenie usuwa aplikację Przykładowa z konta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="a24b9-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="a24b9-110">Polecenie nie powiodło się, jeśli aplikacja zawiera jakieś pakiety.</span><span class="sxs-lookup"><span data-stu-id="a24b9-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="a24b9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a24b9-111">PARAMETERS</span></span>

### <span data-ttu-id="a24b9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a24b9-112">-AccountName</span></span>
<span data-ttu-id="a24b9-113">Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa aplikację.</span><span class="sxs-lookup"><span data-stu-id="a24b9-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="a24b9-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="a24b9-114">-ApplicationId</span></span>
<span data-ttu-id="a24b9-115">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a24b9-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="a24b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24b9-116">-DefaultProfile</span></span>
<span data-ttu-id="a24b9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a24b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="a24b9-119">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="a24b9-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a24b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24b9-120">CommonParameters</span></span>
<span data-ttu-id="a24b9-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24b9-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24b9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24b9-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a24b9-123">INPUTS</span></span>

### <span data-ttu-id="a24b9-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a24b9-124">None</span></span>
<span data-ttu-id="a24b9-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a24b9-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a24b9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a24b9-126">OUTPUTS</span></span>

## <span data-ttu-id="a24b9-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a24b9-127">NOTES</span></span>

## <span data-ttu-id="a24b9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a24b9-128">RELATED LINKS</span></span>

[<span data-ttu-id="a24b9-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a24b9-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a24b9-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a24b9-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a24b9-131">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a24b9-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="a24b9-132">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a24b9-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a24b9-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a24b9-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a24b9-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a24b9-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


