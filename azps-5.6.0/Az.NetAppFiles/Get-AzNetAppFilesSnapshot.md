---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 80d8a27aaf0d2aa27f9924d93669548c1d0dda93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968593"
---
# <span data-ttu-id="30a50-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="30a50-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="30a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a50-102">SYNOPSIS</span></span>
<span data-ttu-id="30a50-103">Pobiera szczegółowe informacje o migawki plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="30a50-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="30a50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30a50-104">SYNTAX</span></span>

### <span data-ttu-id="30a50-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="30a50-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30a50-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a50-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30a50-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a50-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a50-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="30a50-108">DESCRIPTION</span></span>
<span data-ttu-id="30a50-109">Polecenie **cmdlet Get-AzNetAppFilesSnapshot** pobiera szczegóły migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="30a50-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="30a50-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30a50-110">EXAMPLES</span></span>

### <span data-ttu-id="30a50-111">Przykład 1. Uzyskiwanie migawki ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="30a50-112">To polecenie pobiera migawkę o nazwie MyAnfSnapshot z poziomu woluminu "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="30a50-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="30a50-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a50-113">PARAMETERS</span></span>

### <span data-ttu-id="30a50-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30a50-114">-AccountName</span></span>
<span data-ttu-id="30a50-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="30a50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a50-116">-DefaultProfile</span></span>
<span data-ttu-id="30a50-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30a50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a50-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="30a50-118">-Name</span></span>
<span data-ttu-id="30a50-119">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a50-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="30a50-120">-PoolName</span></span>
<span data-ttu-id="30a50-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="30a50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a50-122">-ResourceGroupName</span></span>
<span data-ttu-id="30a50-123">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="30a50-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a50-124">-ResourceId</span></span>
<span data-ttu-id="30a50-125">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="30a50-126">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="30a50-126">-VolumeName</span></span>
<span data-ttu-id="30a50-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="30a50-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="30a50-128">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="30a50-128">-VolumeObject</span></span>
<span data-ttu-id="30a50-129">Obiekt głośności zawierający migawkę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="30a50-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a50-130">CommonParameters</span></span>
<span data-ttu-id="30a50-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a50-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a50-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a50-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a50-133">INPUTS</span></span>

### <span data-ttu-id="30a50-134">System.String</span><span class="sxs-lookup"><span data-stu-id="30a50-134">System.String</span></span>

### <span data-ttu-id="30a50-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="30a50-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="30a50-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a50-136">OUTPUTS</span></span>

### <span data-ttu-id="30a50-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="30a50-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="30a50-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30a50-138">NOTES</span></span>

## <span data-ttu-id="30a50-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a50-139">RELATED LINKS</span></span>
