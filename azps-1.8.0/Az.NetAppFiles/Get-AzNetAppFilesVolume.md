---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709744"
---
# <span data-ttu-id="6ad83-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6ad83-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="6ad83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ad83-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad83-103">Pobiera szczegółowe informacje o woluminie plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="6ad83-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="6ad83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ad83-104">SYNTAX</span></span>

### <span data-ttu-id="6ad83-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ad83-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad83-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad83-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad83-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad83-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad83-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ad83-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad83-109">Polecenie cmdlet **Get-AzNetAppFilesVolume** pobiera szczegóły woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="6ad83-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="6ad83-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ad83-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad83-111">Przykład 1: uzyskiwanie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="6ad83-112">To polecenie pobiera wolumin o nazwie MyAnfVolume z puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="6ad83-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="6ad83-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ad83-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad83-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ad83-114">-AccountName</span></span>
<span data-ttu-id="6ad83-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad83-116">-DefaultProfile</span></span>
<span data-ttu-id="6ad83-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ad83-118">-Name</span></span>
<span data-ttu-id="6ad83-119">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6ad83-120">-PoolName</span></span>
<span data-ttu-id="6ad83-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-122">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="6ad83-122">-PoolObject</span></span>
<span data-ttu-id="6ad83-123">Obiekt Pool zawierający wolumin do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="6ad83-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad83-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ad83-125">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-125">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad83-126">-ResourceId</span></span>
<span data-ttu-id="6ad83-127">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6ad83-127">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad83-128">CommonParameters</span></span>
<span data-ttu-id="6ad83-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ad83-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad83-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad83-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad83-131">INPUTS</span></span>

### <span data-ttu-id="6ad83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad83-132">System.String</span></span>

### <span data-ttu-id="6ad83-133">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6ad83-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6ad83-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ad83-134">OUTPUTS</span></span>

### <span data-ttu-id="6ad83-135">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6ad83-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6ad83-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ad83-136">NOTES</span></span>

## <span data-ttu-id="6ad83-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad83-137">RELATED LINKS</span></span>
