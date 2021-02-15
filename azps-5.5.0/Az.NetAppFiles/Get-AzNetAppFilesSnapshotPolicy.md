---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203325"
---
# <span data-ttu-id="59108-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="59108-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="59108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59108-102">SYNOPSIS</span></span>
<span data-ttu-id="59108-103">Pobiera szczegółowe informacje o zasadach migawki plików AZURE NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="59108-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="59108-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59108-104">SYNTAX</span></span>

### <span data-ttu-id="59108-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="59108-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59108-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59108-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59108-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59108-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59108-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="59108-108">DESCRIPTION</span></span>
<span data-ttu-id="59108-109">Polecenie **cmdlet Get-AzNetAppFilesSnapshotPolicy** pobiera szczegółowe informacje o zasadach migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="59108-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="59108-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59108-110">EXAMPLES</span></span>

### <span data-ttu-id="59108-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59108-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="59108-112">To polecenie pobiera zasady kopii zapasowej o nazwie "MyBackupPolicy" dla konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="59108-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="59108-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59108-113">PARAMETERS</span></span>

### <span data-ttu-id="59108-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59108-114">-AccountName</span></span>
<span data-ttu-id="59108-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="59108-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59108-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="59108-116">-AccountObject</span></span>
<span data-ttu-id="59108-117">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="59108-117">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59108-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59108-118">-DefaultProfile</span></span>
<span data-ttu-id="59108-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59108-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59108-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59108-120">-Name</span></span>
<span data-ttu-id="59108-121">Nazwa zasad migawki ANF</span><span class="sxs-lookup"><span data-stu-id="59108-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59108-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59108-122">-ResourceGroupName</span></span>
<span data-ttu-id="59108-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="59108-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59108-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59108-124">-ResourceId</span></span>
<span data-ttu-id="59108-125">Identyfikator zasobu zasad migawki ANF</span><span class="sxs-lookup"><span data-stu-id="59108-125">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59108-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59108-126">-Confirm</span></span>
<span data-ttu-id="59108-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59108-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59108-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59108-128">-WhatIf</span></span>
<span data-ttu-id="59108-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59108-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59108-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59108-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59108-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59108-131">CommonParameters</span></span>
<span data-ttu-id="59108-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59108-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59108-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59108-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59108-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59108-134">INPUTS</span></span>

### <span data-ttu-id="59108-135">System.String</span><span class="sxs-lookup"><span data-stu-id="59108-135">System.String</span></span>

### <span data-ttu-id="59108-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="59108-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="59108-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59108-137">OUTPUTS</span></span>

### <span data-ttu-id="59108-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="59108-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="59108-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59108-139">NOTES</span></span>

## <span data-ttu-id="59108-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59108-140">RELATED LINKS</span></span>
