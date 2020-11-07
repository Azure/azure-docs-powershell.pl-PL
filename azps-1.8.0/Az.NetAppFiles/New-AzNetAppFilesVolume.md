---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709736"
---
# <span data-ttu-id="05379-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="05379-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="05379-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05379-102">SYNOPSIS</span></span>
<span data-ttu-id="05379-103">Tworzy nowy wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="05379-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="05379-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05379-104">SYNTAX</span></span>

### <span data-ttu-id="05379-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05379-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05379-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05379-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05379-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05379-107">DESCRIPTION</span></span>
<span data-ttu-id="05379-108">Polecenie cmdlet **New-AzNetAppFilesVolume** tworzy wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="05379-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="05379-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05379-109">EXAMPLES</span></span>

### <span data-ttu-id="05379-110">Przykład 1. Tworzenie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="05379-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="05379-111">To polecenie tworzy nowy wolumin ANF "MyAnfVolume" w puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="05379-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="05379-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05379-112">PARAMETERS</span></span>

### <span data-ttu-id="05379-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="05379-113">-AccountName</span></span>
<span data-ttu-id="05379-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="05379-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="05379-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="05379-115">-CreationToken</span></span>
<span data-ttu-id="05379-116">Unikatowa ścieżka pliku dla woluminu</span><span class="sxs-lookup"><span data-stu-id="05379-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05379-117">-DefaultProfile</span></span>
<span data-ttu-id="05379-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05379-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05379-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="05379-119">-Location</span></span>
<span data-ttu-id="05379-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="05379-120">The location of the resource</span></span>

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

### <span data-ttu-id="05379-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05379-121">-Name</span></span>
<span data-ttu-id="05379-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="05379-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="05379-123">-PoolName</span></span>
<span data-ttu-id="05379-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="05379-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="05379-125">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="05379-125">-PoolObject</span></span>
<span data-ttu-id="05379-126">Pula dla nowego obiektu woluminu</span><span class="sxs-lookup"><span data-stu-id="05379-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="05379-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05379-127">-ResourceGroupName</span></span>
<span data-ttu-id="05379-128">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="05379-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="05379-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="05379-129">-ServiceLevel</span></span>
<span data-ttu-id="05379-130">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="05379-130">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="05379-131">-SubnetId</span></span>
<span data-ttu-id="05379-132">Identyfikator URI zasobu platformy Azure dla delegowanej podsieci</span><span class="sxs-lookup"><span data-stu-id="05379-132">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="05379-133">-Tag</span></span>
<span data-ttu-id="05379-134">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="05379-134">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="05379-135">-UsageThreshold</span></span>
<span data-ttu-id="05379-136">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="05379-136">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05379-137">-Confirm</span></span>
<span data-ttu-id="05379-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05379-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05379-139">-WhatIf</span></span>
<span data-ttu-id="05379-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05379-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05379-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05379-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05379-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05379-142">CommonParameters</span></span>
<span data-ttu-id="05379-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05379-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="05379-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05379-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05379-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05379-145">INPUTS</span></span>

### <span data-ttu-id="05379-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="05379-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="05379-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05379-147">OUTPUTS</span></span>

### <span data-ttu-id="05379-148">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="05379-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="05379-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05379-149">NOTES</span></span>

## <span data-ttu-id="05379-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05379-150">RELATED LINKS</span></span>
