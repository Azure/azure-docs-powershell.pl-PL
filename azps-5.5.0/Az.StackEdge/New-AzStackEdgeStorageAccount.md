---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187866"
---
# <span data-ttu-id="e565f-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e565f-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e565f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e565f-102">SYNOPSIS</span></span>
<span data-ttu-id="e565f-103">Tworzy nowe konto magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="e565f-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="e565f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e565f-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e565f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e565f-105">DESCRIPTION</span></span>
<span data-ttu-id="e565f-106">Polecenie **cmdlet New-AzStackEdgeStorageAccount** tworzy nowe konto magazynu edge na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="e565f-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="e565f-107">W przypadku urządzenia jedno konto magazynu w chmurze można zamapować co najwyżej na jedno konto magazynu w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e565f-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="e565f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e565f-108">EXAMPLES</span></span>

### <span data-ttu-id="e565f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e565f-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="e565f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e565f-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="e565f-111">2 Konta Microsoft EdgeStorageAccounts na urządzeniu nie mogą udostępniać więcej niż 1 konta magazynu w chmurze</span><span class="sxs-lookup"><span data-stu-id="e565f-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="e565f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e565f-112">PARAMETERS</span></span>

### <span data-ttu-id="e565f-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e565f-113">-AsJob</span></span>
<span data-ttu-id="e565f-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e565f-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e565f-115">— Chmura</span><span class="sxs-lookup"><span data-stu-id="e565f-115">-Cloud</span></span>
<span data-ttu-id="e565f-116">Użyje konta CloudStorageAccount do warstwowania</span><span class="sxs-lookup"><span data-stu-id="e565f-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e565f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e565f-117">-DefaultProfile</span></span>
<span data-ttu-id="e565f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e565f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e565f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e565f-119">-DeviceName</span></span>
<span data-ttu-id="e565f-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="e565f-120">Device Name</span></span>

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

### <span data-ttu-id="e565f-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e565f-121">-Name</span></span>
<span data-ttu-id="e565f-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="e565f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e565f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e565f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e565f-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e565f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e565f-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="e565f-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="e565f-126">Podaj nazwę istniejącego zasobu StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e565f-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e565f-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e565f-127">-Confirm</span></span>
<span data-ttu-id="e565f-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e565f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e565f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e565f-129">-WhatIf</span></span>
<span data-ttu-id="e565f-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e565f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e565f-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e565f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e565f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e565f-132">CommonParameters</span></span>
<span data-ttu-id="e565f-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e565f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e565f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e565f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e565f-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e565f-135">INPUTS</span></span>

### <span data-ttu-id="e565f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e565f-136">System.String</span></span>

### <span data-ttu-id="e565f-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e565f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e565f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e565f-138">OUTPUTS</span></span>

### <span data-ttu-id="e565f-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e565f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e565f-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e565f-140">NOTES</span></span>

## <span data-ttu-id="e565f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e565f-141">RELATED LINKS</span></span>
