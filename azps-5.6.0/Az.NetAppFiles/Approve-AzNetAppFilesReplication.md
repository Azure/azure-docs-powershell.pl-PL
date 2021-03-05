---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: ac562f95ad6d5cbc97e31cd3832b90d2aa2362e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968698"
---
# <span data-ttu-id="ed482-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ed482-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ed482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed482-102">SYNOPSIS</span></span>
<span data-ttu-id="ed482-103">Zatwierdzanie/autoryzowanie połączenia replikacji w woluminie źródłowym</span><span class="sxs-lookup"><span data-stu-id="ed482-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="ed482-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed482-104">SYNTAX</span></span>

### <span data-ttu-id="ed482-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ed482-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed482-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed482-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed482-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed482-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed482-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed482-108">DESCRIPTION</span></span>
<span data-ttu-id="ed482-109">Zatwierdzanie połączenia replikacji w woluminie źródłowym</span><span class="sxs-lookup"><span data-stu-id="ed482-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="ed482-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed482-110">EXAMPLES</span></span>

### <span data-ttu-id="ed482-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed482-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="ed482-112">To polecenie zatwierdza replikację w umyśle MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="ed482-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="ed482-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed482-113">PARAMETERS</span></span>

### <span data-ttu-id="ed482-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed482-114">-AccountName</span></span>
<span data-ttu-id="ed482-115">Nazwa konta ANF woluminu źródła replikacji</span><span class="sxs-lookup"><span data-stu-id="ed482-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="ed482-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="ed482-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="ed482-117">Identyfikator systemu plików woluminu ochrony danych docelowych</span><span class="sxs-lookup"><span data-stu-id="ed482-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="ed482-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed482-118">-DefaultProfile</span></span>
<span data-ttu-id="ed482-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed482-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed482-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed482-120">-InputObject</span></span>
<span data-ttu-id="ed482-121">Obiekt głośności źródła ANF do autoryzacji miejsca docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="ed482-121">The ANF source volume object to authorized the replication destination</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed482-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed482-122">-Name</span></span>
<span data-ttu-id="ed482-123">Nazwa woluminu źródła replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ed482-123">The name of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed482-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed482-124">-PassThru</span></span>
<span data-ttu-id="ed482-125">Zwracanie, czy wykonano autoryzację replikacji dla określonego woluminu</span><span class="sxs-lookup"><span data-stu-id="ed482-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="ed482-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ed482-126">-PoolName</span></span>
<span data-ttu-id="ed482-127">Nazwa puli ANF dla woluminu źródła replikacji</span><span class="sxs-lookup"><span data-stu-id="ed482-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="ed482-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed482-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed482-129">Grupa zasobów woluminu źródła replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ed482-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="ed482-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed482-130">-ResourceId</span></span>
<span data-ttu-id="ed482-131">Identyfikator zasobu woluminu źródła replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ed482-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="ed482-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed482-132">-Confirm</span></span>
<span data-ttu-id="ed482-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ed482-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed482-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed482-134">-WhatIf</span></span>
<span data-ttu-id="ed482-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed482-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed482-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ed482-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed482-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed482-137">CommonParameters</span></span>
<span data-ttu-id="ed482-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed482-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed482-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed482-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed482-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed482-140">INPUTS</span></span>

### <span data-ttu-id="ed482-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ed482-141">System.String</span></span>

### <span data-ttu-id="ed482-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ed482-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ed482-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed482-143">OUTPUTS</span></span>

### <span data-ttu-id="ed482-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed482-144">System.Boolean</span></span>

## <span data-ttu-id="ed482-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed482-145">NOTES</span></span>

## <span data-ttu-id="ed482-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed482-146">RELATED LINKS</span></span>
