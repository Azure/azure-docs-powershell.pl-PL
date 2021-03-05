---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: c0cea590ced7abdaad1021453304ea1508790b55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978602"
---
# <span data-ttu-id="cf02d-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf02d-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="cf02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf02d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf02d-103">Tworzy nowe konto magazynu edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="cf02d-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="cf02d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf02d-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf02d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf02d-105">DESCRIPTION</span></span>
<span data-ttu-id="cf02d-106">Polecenie **cmdlet New-AzDataBoxEdgeStorageAccount** tworzy nowe konto magazynu edge na urządzeniu z programem Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="cf02d-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="cf02d-107">W przypadku urządzenia jedno konto magazynu w chmurze można zamapować co najwyżej na jedno konto magazynu w chmurze.</span><span class="sxs-lookup"><span data-stu-id="cf02d-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="cf02d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf02d-108">EXAMPLES</span></span>

### <span data-ttu-id="cf02d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf02d-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="cf02d-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cf02d-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="cf02d-111">2 Konta Microsoft EdgeStorageAccounts na urządzeniu nie mogą udostępniać więcej niż 1 konta magazynu w chmurze</span><span class="sxs-lookup"><span data-stu-id="cf02d-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="cf02d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf02d-112">PARAMETERS</span></span>

### <span data-ttu-id="cf02d-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cf02d-113">-AsJob</span></span>
<span data-ttu-id="cf02d-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cf02d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf02d-115">— Chmura</span><span class="sxs-lookup"><span data-stu-id="cf02d-115">-Cloud</span></span>
<span data-ttu-id="cf02d-116">Użyje konta CloudStorageAccount do warstwowania</span><span class="sxs-lookup"><span data-stu-id="cf02d-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="cf02d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf02d-117">-DefaultProfile</span></span>
<span data-ttu-id="cf02d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf02d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf02d-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cf02d-119">-DeviceName</span></span>
<span data-ttu-id="cf02d-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="cf02d-120">Device Name</span></span>

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

### <span data-ttu-id="cf02d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf02d-121">-Name</span></span>
<span data-ttu-id="cf02d-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="cf02d-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf02d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf02d-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf02d-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cf02d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cf02d-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="cf02d-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="cf02d-126">Podaj nazwę istniejącego zasobu StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cf02d-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="cf02d-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf02d-127">-Confirm</span></span>
<span data-ttu-id="cf02d-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf02d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf02d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf02d-129">-WhatIf</span></span>
<span data-ttu-id="cf02d-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf02d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf02d-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf02d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf02d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf02d-132">CommonParameters</span></span>
<span data-ttu-id="cf02d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf02d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf02d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf02d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf02d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf02d-135">INPUTS</span></span>

### <span data-ttu-id="cf02d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cf02d-136">System.String</span></span>

### <span data-ttu-id="cf02d-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="cf02d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf02d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf02d-138">OUTPUTS</span></span>

### <span data-ttu-id="cf02d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf02d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="cf02d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf02d-140">NOTES</span></span>

## <span data-ttu-id="cf02d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf02d-141">RELATED LINKS</span></span>
