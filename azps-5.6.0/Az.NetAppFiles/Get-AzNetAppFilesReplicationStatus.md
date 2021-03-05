---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: 73efd000f6889675c3daf9f99821640a8b6fbb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968609"
---
# <span data-ttu-id="eef39-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="eef39-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="eef39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef39-102">SYNOPSIS</span></span>
<span data-ttu-id="eef39-103">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="eef39-103">Get the status of the replication</span></span>

## <span data-ttu-id="eef39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eef39-104">SYNTAX</span></span>

### <span data-ttu-id="eef39-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="eef39-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eef39-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eef39-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eef39-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eef39-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef39-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="eef39-108">DESCRIPTION</span></span>
<span data-ttu-id="eef39-109">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="eef39-109">Get the status of the replication</span></span>

## <span data-ttu-id="eef39-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eef39-110">EXAMPLES</span></span>

### <span data-ttu-id="eef39-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eef39-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="eef39-112">To polecenie otrzymuje stan replikacji na myvol</span><span class="sxs-lookup"><span data-stu-id="eef39-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="eef39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef39-113">PARAMETERS</span></span>

### <span data-ttu-id="eef39-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eef39-114">-AccountName</span></span>
<span data-ttu-id="eef39-115">Nazwa konta ANF woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="eef39-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="eef39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef39-116">-DefaultProfile</span></span>
<span data-ttu-id="eef39-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eef39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef39-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eef39-118">-InputObject</span></span>
<span data-ttu-id="eef39-119">Obiekt obrotu miejsca docelowego replikacji ANF w celu uzyskania stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="eef39-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="eef39-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eef39-120">-Name</span></span>
<span data-ttu-id="eef39-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="eef39-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eef39-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="eef39-122">-PoolName</span></span>
<span data-ttu-id="eef39-123">Nazwa puli ANF dla woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="eef39-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="eef39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef39-124">-ResourceGroupName</span></span>
<span data-ttu-id="eef39-125">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="eef39-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eef39-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eef39-126">-ResourceId</span></span>
<span data-ttu-id="eef39-127">Identyfikator zasobu woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="eef39-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eef39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef39-128">CommonParameters</span></span>
<span data-ttu-id="eef39-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef39-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef39-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef39-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eef39-131">INPUTS</span></span>

### <span data-ttu-id="eef39-132">System.String</span><span class="sxs-lookup"><span data-stu-id="eef39-132">System.String</span></span>

### <span data-ttu-id="eef39-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eef39-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="eef39-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eef39-134">OUTPUTS</span></span>

### <span data-ttu-id="eef39-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="eef39-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="eef39-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eef39-136">NOTES</span></span>

## <span data-ttu-id="eef39-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eef39-137">RELATED LINKS</span></span>
