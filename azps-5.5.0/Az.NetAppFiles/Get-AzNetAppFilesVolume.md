---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184874"
---
# <span data-ttu-id="47350-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="47350-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="47350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47350-102">SYNOPSIS</span></span>
<span data-ttu-id="47350-103">Pobiera szczegółowe informacje o ilości plików Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="47350-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="47350-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47350-104">SYNTAX</span></span>

### <span data-ttu-id="47350-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="47350-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47350-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47350-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47350-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47350-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47350-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="47350-108">DESCRIPTION</span></span>
<span data-ttu-id="47350-109">Polecenie **cmdlet Get-AzNetAppFilesVolume** pobiera szczegóły dotyczące woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="47350-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="47350-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47350-110">EXAMPLES</span></span>

### <span data-ttu-id="47350-111">Przykład 1. Uzyskiwanie głośności ANF</span><span class="sxs-lookup"><span data-stu-id="47350-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="47350-112">To polecenie pobiera wolumin o nazwie MyAnfVolume z puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="47350-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="47350-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47350-113">PARAMETERS</span></span>

### <span data-ttu-id="47350-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47350-114">-AccountName</span></span>
<span data-ttu-id="47350-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="47350-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="47350-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47350-116">-DefaultProfile</span></span>
<span data-ttu-id="47350-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47350-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47350-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47350-118">-Name</span></span>
<span data-ttu-id="47350-119">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="47350-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47350-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="47350-120">-PoolName</span></span>
<span data-ttu-id="47350-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="47350-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="47350-122">- PoolObject</span><span class="sxs-lookup"><span data-stu-id="47350-122">-PoolObject</span></span>
<span data-ttu-id="47350-123">Obiekt puli zawierający wielkość, która ma być zwracana</span><span class="sxs-lookup"><span data-stu-id="47350-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47350-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47350-124">-ResourceGroupName</span></span>
<span data-ttu-id="47350-125">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="47350-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="47350-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47350-126">-ResourceId</span></span>
<span data-ttu-id="47350-127">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="47350-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="47350-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47350-128">CommonParameters</span></span>
<span data-ttu-id="47350-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47350-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47350-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47350-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47350-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47350-131">INPUTS</span></span>

### <span data-ttu-id="47350-132">System.String</span><span class="sxs-lookup"><span data-stu-id="47350-132">System.String</span></span>

### <span data-ttu-id="47350-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="47350-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="47350-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47350-134">OUTPUTS</span></span>

### <span data-ttu-id="47350-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="47350-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="47350-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47350-136">NOTES</span></span>

## <span data-ttu-id="47350-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47350-137">RELATED LINKS</span></span>
