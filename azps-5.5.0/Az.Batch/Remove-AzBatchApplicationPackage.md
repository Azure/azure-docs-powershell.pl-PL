---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197018"
---
# <span data-ttu-id="68b50-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68b50-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="68b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b50-102">SYNOPSIS</span></span>
<span data-ttu-id="68b50-103">Usuwa rekord pakietu aplikacji i plik binarny.</span><span class="sxs-lookup"><span data-stu-id="68b50-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="68b50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68b50-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68b50-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="68b50-105">DESCRIPTION</span></span>
<span data-ttu-id="68b50-106">Polecenie **cmdlet Remove-AzBatchApplicationPackage** usuwa rekord pakietu aplikacji i plik binarny z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="68b50-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="68b50-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68b50-107">EXAMPLES</span></span>

### <span data-ttu-id="68b50-108">Przykład 1. Usuwanie pakietu aplikacji z konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="68b50-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="68b50-109">To polecenie usuwa wersję 1.0 aplikacji Litware z konta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="68b50-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="68b50-110">Polecenie usuwa zarówno rekord pakietu, jak i obiekt blob, który zawiera plik binarny pakietu.</span><span class="sxs-lookup"><span data-stu-id="68b50-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="68b50-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68b50-111">PARAMETERS</span></span>

### <span data-ttu-id="68b50-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68b50-112">-AccountName</span></span>
<span data-ttu-id="68b50-113">Określa nazwę konta usługi Batch, z którego to polecenie cmdlet usuwa pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="68b50-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="68b50-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="68b50-114">-ApplicationName</span></span>
<span data-ttu-id="68b50-115">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="68b50-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="68b50-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="68b50-116">-ApplicationVersion</span></span>
<span data-ttu-id="68b50-117">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="68b50-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="68b50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b50-118">-DefaultProfile</span></span>
<span data-ttu-id="68b50-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="68b50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68b50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b50-120">-ResourceGroupName</span></span>
<span data-ttu-id="68b50-121">Określa nazwę grupy zasobów zawierającej konto Batch.</span><span class="sxs-lookup"><span data-stu-id="68b50-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="68b50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b50-122">CommonParameters</span></span>
<span data-ttu-id="68b50-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b50-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68b50-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b50-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68b50-125">INPUTS</span></span>

### <span data-ttu-id="68b50-126">System.String</span><span class="sxs-lookup"><span data-stu-id="68b50-126">System.String</span></span>

## <span data-ttu-id="68b50-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68b50-127">OUTPUTS</span></span>

### <span data-ttu-id="68b50-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="68b50-128">System.Void</span></span>

## <span data-ttu-id="68b50-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68b50-129">NOTES</span></span>

## <span data-ttu-id="68b50-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68b50-130">RELATED LINKS</span></span>

[<span data-ttu-id="68b50-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68b50-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="68b50-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68b50-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="68b50-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68b50-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="68b50-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="68b50-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="68b50-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68b50-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="68b50-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="68b50-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


