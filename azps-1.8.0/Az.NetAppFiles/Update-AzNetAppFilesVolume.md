---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709724"
---
# <span data-ttu-id="c4065-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c4065-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c4065-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4065-102">SYNOPSIS</span></span>
<span data-ttu-id="c4065-103">Aktualizuje wolumin pliki usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="c4065-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c4065-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4065-104">SYNTAX</span></span>

### <span data-ttu-id="c4065-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4065-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4065-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4065-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4065-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4065-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4065-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4065-108">DESCRIPTION</span></span>
<span data-ttu-id="c4065-109">Polecenie cmdlet **Update-AzNetAppFilesVolume** AKTUALIZUJE wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="c4065-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="c4065-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4065-110">EXAMPLES</span></span>

### <span data-ttu-id="c4065-111">Przykład 1: aktualizowanie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-111">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="c4065-112">To polecenie aktualizuje wolumin ANF "MyAnfVolume" przy użyciu nowego rozmiaru UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="c4065-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="c4065-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4065-113">PARAMETERS</span></span>

### <span data-ttu-id="c4065-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4065-114">-AccountName</span></span>
<span data-ttu-id="c4065-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="c4065-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4065-116">-DefaultProfile</span></span>
<span data-ttu-id="c4065-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4065-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4065-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4065-118">-InputObject</span></span>
<span data-ttu-id="c4065-119">Obiekt woluminu do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="c4065-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4065-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c4065-120">-Location</span></span>
<span data-ttu-id="c4065-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="c4065-121">The location of the resource</span></span>

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

### <span data-ttu-id="c4065-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4065-122">-Name</span></span>
<span data-ttu-id="c4065-123">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4065-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c4065-124">-PoolName</span></span>
<span data-ttu-id="c4065-125">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c4065-126">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="c4065-126">-PoolObject</span></span>
<span data-ttu-id="c4065-127">Obiekt Pool zawierający wolumin do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="c4065-127">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="c4065-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4065-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4065-129">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c4065-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c4065-130">-ServiceLevel</span></span>
<span data-ttu-id="c4065-131">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="c4065-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4065-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4065-132">-Tag</span></span>
<span data-ttu-id="c4065-133">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="c4065-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c4065-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="c4065-134">-UsageThreshold</span></span>
<span data-ttu-id="c4065-135">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="c4065-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4065-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4065-136">-Confirm</span></span>
<span data-ttu-id="c4065-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4065-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4065-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4065-138">-WhatIf</span></span>
<span data-ttu-id="c4065-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4065-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4065-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4065-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4065-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4065-141">CommonParameters</span></span>
<span data-ttu-id="c4065-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4065-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c4065-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4065-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4065-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4065-144">INPUTS</span></span>

### <span data-ttu-id="c4065-145">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c4065-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c4065-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c4065-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c4065-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4065-147">OUTPUTS</span></span>

### <span data-ttu-id="c4065-148">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c4065-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c4065-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4065-149">NOTES</span></span>

## <span data-ttu-id="c4065-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4065-150">RELATED LINKS</span></span>
