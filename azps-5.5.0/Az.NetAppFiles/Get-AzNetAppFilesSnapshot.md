---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241147"
---
# <span data-ttu-id="d91b9-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d91b9-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d91b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d91b9-103">Pobiera szczegółowe informacje o migawki plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="d91b9-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="d91b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d91b9-104">SYNTAX</span></span>

### <span data-ttu-id="d91b9-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d91b9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d91b9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d91b9-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d91b9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d91b9-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d91b9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d91b9-108">DESCRIPTION</span></span>
<span data-ttu-id="d91b9-109">Polecenie **cmdlet Get-AzNetAppFilesSnapshot** pobiera szczegóły migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="d91b9-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="d91b9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d91b9-110">EXAMPLES</span></span>

### <span data-ttu-id="d91b9-111">Przykład 1. Uzyskiwanie migawki ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-111">Example 1: Get an ANF snapshot</span></span>
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

<span data-ttu-id="d91b9-112">To polecenie pobiera migawkę o nazwie MyAnfSnapshot z poziomu woluminu "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="d91b9-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d91b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d91b9-113">PARAMETERS</span></span>

### <span data-ttu-id="d91b9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d91b9-114">-AccountName</span></span>
<span data-ttu-id="d91b9-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="d91b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91b9-116">-DefaultProfile</span></span>
<span data-ttu-id="d91b9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d91b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d91b9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d91b9-118">-Name</span></span>
<span data-ttu-id="d91b9-119">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-119">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="d91b9-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d91b9-120">-PoolName</span></span>
<span data-ttu-id="d91b9-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d91b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="d91b9-123">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="d91b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d91b9-124">-ResourceId</span></span>
<span data-ttu-id="d91b9-125">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="d91b9-126">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="d91b9-126">-VolumeName</span></span>
<span data-ttu-id="d91b9-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d91b9-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d91b9-128">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="d91b9-128">-VolumeObject</span></span>
<span data-ttu-id="d91b9-129">Obiekt głośności zawierający migawkę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="d91b9-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="d91b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91b9-130">CommonParameters</span></span>
<span data-ttu-id="d91b9-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91b9-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d91b9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91b9-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d91b9-133">INPUTS</span></span>

### <span data-ttu-id="d91b9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d91b9-134">System.String</span></span>

### <span data-ttu-id="d91b9-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d91b9-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d91b9-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d91b9-136">OUTPUTS</span></span>

### <span data-ttu-id="d91b9-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d91b9-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d91b9-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d91b9-138">NOTES</span></span>

## <span data-ttu-id="d91b9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d91b9-139">RELATED LINKS</span></span>
