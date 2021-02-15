---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195242"
---
# <span data-ttu-id="5b3e1-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b3e1-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="5b3e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3e1-103">Usuwa aplikację z konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="5b3e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b3e1-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b3e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="5b3e1-106">Polecenie **cmdlet Remove-AzBatchApplication** usuwa aplikację z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="5b3e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b3e1-107">EXAMPLES</span></span>

### <span data-ttu-id="5b3e1-108">Przykład 1. Usuwanie aplikacji z konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="5b3e1-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="5b3e1-109">To polecenie usuwa aplikację Litware z konta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="5b3e1-110">To polecenie kończy się niepowodzeniem, jeśli aplikacja zawiera jakiekolwiek pakiety.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="5b3e1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b3e1-111">PARAMETERS</span></span>

### <span data-ttu-id="5b3e1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b3e1-112">-AccountName</span></span>
<span data-ttu-id="5b3e1-113">Określa nazwę konta usługi Batch, z którego to polecenie cmdlet usuwa aplikację.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="5b3e1-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5b3e1-114">-ApplicationName</span></span>
<span data-ttu-id="5b3e1-115">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3e1-116">-DefaultProfile</span></span>
<span data-ttu-id="5b3e1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b3e1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3e1-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b3e1-119">Określa nazwę grupy zasobów zawierającej konto batch.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="5b3e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3e1-120">CommonParameters</span></span>
<span data-ttu-id="5b3e1-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3e1-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b3e1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3e1-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b3e1-123">INPUTS</span></span>

### <span data-ttu-id="5b3e1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5b3e1-124">System.String</span></span>

## <span data-ttu-id="5b3e1-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b3e1-125">OUTPUTS</span></span>

### <span data-ttu-id="5b3e1-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="5b3e1-126">System.Void</span></span>

## <span data-ttu-id="5b3e1-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b3e1-127">NOTES</span></span>

## <span data-ttu-id="5b3e1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b3e1-128">RELATED LINKS</span></span>

[<span data-ttu-id="5b3e1-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b3e1-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="5b3e1-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b3e1-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b3e1-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b3e1-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="5b3e1-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b3e1-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b3e1-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b3e1-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b3e1-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b3e1-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


