---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232080"
---
# <span data-ttu-id="443eb-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="443eb-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="443eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="443eb-102">SYNOPSIS</span></span>
<span data-ttu-id="443eb-103">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="443eb-103">Get the status of the replication</span></span>

## <span data-ttu-id="443eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="443eb-104">SYNTAX</span></span>

### <span data-ttu-id="443eb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="443eb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="443eb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="443eb-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="443eb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="443eb-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="443eb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="443eb-108">DESCRIPTION</span></span>
<span data-ttu-id="443eb-109">Uzyskiwanie stanu replikacji</span><span class="sxs-lookup"><span data-stu-id="443eb-109">Get the status of the replication</span></span>

## <span data-ttu-id="443eb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="443eb-110">EXAMPLES</span></span>

### <span data-ttu-id="443eb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="443eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="443eb-112">To polecenie uzyskuje stan replikacji na MyVol</span><span class="sxs-lookup"><span data-stu-id="443eb-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="443eb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="443eb-113">PARAMETERS</span></span>

### <span data-ttu-id="443eb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="443eb-114">-AccountName</span></span>
<span data-ttu-id="443eb-115">Nazwa konta ANF woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="443eb-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="443eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443eb-116">-DefaultProfile</span></span>
<span data-ttu-id="443eb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="443eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="443eb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="443eb-118">-InputObject</span></span>
<span data-ttu-id="443eb-119">Obiekt woluminu docelowego replikacji ANF, aby uzyskać stan replikacji</span><span class="sxs-lookup"><span data-stu-id="443eb-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="443eb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="443eb-120">-Name</span></span>
<span data-ttu-id="443eb-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="443eb-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="443eb-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="443eb-122">-PoolName</span></span>
<span data-ttu-id="443eb-123">Nazwa puli ANF woluminu docelowego replikacji</span><span class="sxs-lookup"><span data-stu-id="443eb-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="443eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="443eb-125">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="443eb-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="443eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="443eb-126">-ResourceId</span></span>
<span data-ttu-id="443eb-127">Identyfikator zasobu w docelowym woluminie replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="443eb-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="443eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443eb-128">CommonParameters</span></span>
<span data-ttu-id="443eb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="443eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443eb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="443eb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443eb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="443eb-131">INPUTS</span></span>

### <span data-ttu-id="443eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="443eb-132">System.String</span></span>

## <span data-ttu-id="443eb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="443eb-133">OUTPUTS</span></span>

### <span data-ttu-id="443eb-134">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="443eb-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="443eb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="443eb-135">NOTES</span></span>

## <span data-ttu-id="443eb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="443eb-136">RELATED LINKS</span></span>
