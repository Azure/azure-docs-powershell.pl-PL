---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710425"
---
# <span data-ttu-id="31b60-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31b60-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="31b60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31b60-102">SYNOPSIS</span></span>
<span data-ttu-id="31b60-103">Usuwa aplikację z konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="31b60-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="31b60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31b60-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31b60-105">DESCRIPTION</span></span>
<span data-ttu-id="31b60-106">Polecenie cmdlet **Remove-AzBatchApplication** usuwa aplikację z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="31b60-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="31b60-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31b60-107">EXAMPLES</span></span>

### <span data-ttu-id="31b60-108">Przykład 1: Usuwanie aplikacji z konta partii</span><span class="sxs-lookup"><span data-stu-id="31b60-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="31b60-109">To polecenie usuwa aplikację Przykładowa z konta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="31b60-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="31b60-110">Polecenie nie powiodło się, jeśli aplikacja zawiera jakieś pakiety.</span><span class="sxs-lookup"><span data-stu-id="31b60-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="31b60-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31b60-111">PARAMETERS</span></span>

### <span data-ttu-id="31b60-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31b60-112">-AccountName</span></span>
<span data-ttu-id="31b60-113">Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa aplikację.</span><span class="sxs-lookup"><span data-stu-id="31b60-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="31b60-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="31b60-114">-ApplicationId</span></span>
<span data-ttu-id="31b60-115">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="31b60-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="31b60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b60-116">-DefaultProfile</span></span>
<span data-ttu-id="31b60-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31b60-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b60-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b60-118">-ResourceGroupName</span></span>
<span data-ttu-id="31b60-119">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="31b60-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="31b60-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b60-120">CommonParameters</span></span>
<span data-ttu-id="31b60-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b60-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b60-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b60-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b60-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31b60-123">INPUTS</span></span>

### <span data-ttu-id="31b60-124">System. String</span><span class="sxs-lookup"><span data-stu-id="31b60-124">System.String</span></span>

## <span data-ttu-id="31b60-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31b60-125">OUTPUTS</span></span>

### <span data-ttu-id="31b60-126">System. void</span><span class="sxs-lookup"><span data-stu-id="31b60-126">System.Void</span></span>

## <span data-ttu-id="31b60-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31b60-127">NOTES</span></span>

## <span data-ttu-id="31b60-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31b60-128">RELATED LINKS</span></span>

[<span data-ttu-id="31b60-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31b60-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="31b60-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31b60-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="31b60-131">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31b60-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="31b60-132">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31b60-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="31b60-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31b60-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="31b60-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31b60-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


