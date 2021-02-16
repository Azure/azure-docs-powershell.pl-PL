---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192075"
---
# <span data-ttu-id="ffb68-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ffb68-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ffb68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb68-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb68-103">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="ffb68-103">Get the status of the replication</span></span>

## <span data-ttu-id="ffb68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ffb68-104">SYNTAX</span></span>

### <span data-ttu-id="ffb68-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ffb68-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffb68-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffb68-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffb68-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffb68-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffb68-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ffb68-108">DESCRIPTION</span></span>
<span data-ttu-id="ffb68-109">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="ffb68-109">Get the status of the replication</span></span>

## <span data-ttu-id="ffb68-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ffb68-110">EXAMPLES</span></span>

### <span data-ttu-id="ffb68-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffb68-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="ffb68-112">To polecenie otrzymuje stan replikacji na myvol</span><span class="sxs-lookup"><span data-stu-id="ffb68-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="ffb68-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffb68-113">PARAMETERS</span></span>

### <span data-ttu-id="ffb68-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffb68-114">-AccountName</span></span>
<span data-ttu-id="ffb68-115">Nazwa konta ANF woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="ffb68-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="ffb68-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb68-116">-DefaultProfile</span></span>
<span data-ttu-id="ffb68-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffb68-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb68-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffb68-118">-InputObject</span></span>
<span data-ttu-id="ffb68-119">Obiekt obrotu miejsca docelowego replikacji ANF w celu uzyskania stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="ffb68-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="ffb68-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ffb68-120">-Name</span></span>
<span data-ttu-id="ffb68-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ffb68-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ffb68-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ffb68-122">-PoolName</span></span>
<span data-ttu-id="ffb68-123">Nazwa puli ANF dla woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="ffb68-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="ffb68-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb68-124">-ResourceGroupName</span></span>
<span data-ttu-id="ffb68-125">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ffb68-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ffb68-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffb68-126">-ResourceId</span></span>
<span data-ttu-id="ffb68-127">Identyfikator zasobu woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="ffb68-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ffb68-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb68-128">CommonParameters</span></span>
<span data-ttu-id="ffb68-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb68-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb68-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffb68-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb68-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffb68-131">INPUTS</span></span>

### <span data-ttu-id="ffb68-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ffb68-132">System.String</span></span>

### <span data-ttu-id="ffb68-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ffb68-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ffb68-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffb68-134">OUTPUTS</span></span>

### <span data-ttu-id="ffb68-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ffb68-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ffb68-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ffb68-136">NOTES</span></span>

## <span data-ttu-id="ffb68-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffb68-137">RELATED LINKS</span></span>
