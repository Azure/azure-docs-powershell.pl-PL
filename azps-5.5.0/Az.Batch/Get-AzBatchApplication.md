---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239418"
---
# <span data-ttu-id="80f88-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="80f88-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="80f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f88-102">SYNOPSIS</span></span>
<span data-ttu-id="80f88-103">Pobiera informacje o określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="80f88-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="80f88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80f88-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f88-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="80f88-105">DESCRIPTION</span></span>
<span data-ttu-id="80f88-106">Polecenie **cmdlet Get-AzBatchApplication** pobiera informacje o aplikacji na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="80f88-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="80f88-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80f88-107">EXAMPLES</span></span>

### <span data-ttu-id="80f88-108">Przykład 1. Wyświetlanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="80f88-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="80f88-109">To polecenie powoduje wyświetlenie wszystkich aplikacji na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="80f88-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="80f88-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80f88-110">PARAMETERS</span></span>

### <span data-ttu-id="80f88-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80f88-111">-AccountName</span></span>
<span data-ttu-id="80f88-112">Określa nazwę konta usługi Batch zawierającego aplikację.</span><span class="sxs-lookup"><span data-stu-id="80f88-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="80f88-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="80f88-113">-ApplicationName</span></span>
<span data-ttu-id="80f88-114">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="80f88-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f88-115">-DefaultProfile</span></span>
<span data-ttu-id="80f88-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80f88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f88-117">-ResourceGroupName</span></span>
<span data-ttu-id="80f88-118">Określa nazwę grupy zasobów zawierającej konto batch.</span><span class="sxs-lookup"><span data-stu-id="80f88-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="80f88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f88-119">CommonParameters</span></span>
<span data-ttu-id="80f88-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f88-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80f88-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f88-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80f88-122">INPUTS</span></span>

### <span data-ttu-id="80f88-123">System.String</span><span class="sxs-lookup"><span data-stu-id="80f88-123">System.String</span></span>

## <span data-ttu-id="80f88-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80f88-124">OUTPUTS</span></span>

### <span data-ttu-id="80f88-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="80f88-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="80f88-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80f88-126">NOTES</span></span>

## <span data-ttu-id="80f88-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80f88-127">RELATED LINKS</span></span>

[<span data-ttu-id="80f88-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="80f88-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="80f88-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="80f88-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="80f88-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="80f88-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="80f88-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="80f88-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="80f88-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="80f88-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="80f88-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="80f88-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


