---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219566"
---
# <span data-ttu-id="85d80-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="85d80-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="85d80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85d80-102">SYNOPSIS</span></span>
<span data-ttu-id="85d80-103">Przywracanie/przywracanie woluminu do jednej z jego migawek</span><span class="sxs-lookup"><span data-stu-id="85d80-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="85d80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85d80-104">SYNTAX</span></span>

### <span data-ttu-id="85d80-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85d80-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85d80-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85d80-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85d80-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85d80-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85d80-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85d80-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85d80-109">Opis</span><span class="sxs-lookup"><span data-stu-id="85d80-109">DESCRIPTION</span></span>
<span data-ttu-id="85d80-110">Przywracanie/przywracanie woluminu do migawki określonej w parametrze SnapshotId</span><span class="sxs-lookup"><span data-stu-id="85d80-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="85d80-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85d80-111">EXAMPLES</span></span>

### <span data-ttu-id="85d80-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85d80-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="85d80-113">To polecenie przywraca/przywraca głośność woluminu do jednej z migawek z snapshotIdą 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="85d80-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="85d80-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85d80-114">PARAMETERS</span></span>

### <span data-ttu-id="85d80-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85d80-115">-AccountName</span></span>
<span data-ttu-id="85d80-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="85d80-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="85d80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d80-117">-DefaultProfile</span></span>
<span data-ttu-id="85d80-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85d80-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85d80-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85d80-119">-InputObject</span></span>
<span data-ttu-id="85d80-120">Obiekt woluminu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="85d80-120">The volume object to remove</span></span>

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

### <span data-ttu-id="85d80-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85d80-121">-Name</span></span>
<span data-ttu-id="85d80-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="85d80-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="85d80-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85d80-123">-PassThru</span></span>
<span data-ttu-id="85d80-124">Zwracanie, czy określony wolumin został pomyślnie przywrócony/przywrócony</span><span class="sxs-lookup"><span data-stu-id="85d80-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d80-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="85d80-125">-PoolName</span></span>
<span data-ttu-id="85d80-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="85d80-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="85d80-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="85d80-127">-PoolObject</span></span>
<span data-ttu-id="85d80-128">Obiekt Pool zawierający wolumin do usunięcia</span><span class="sxs-lookup"><span data-stu-id="85d80-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="85d80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d80-129">-ResourceGroupName</span></span>
<span data-ttu-id="85d80-130">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="85d80-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="85d80-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85d80-131">-ResourceId</span></span>
<span data-ttu-id="85d80-132">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="85d80-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="85d80-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="85d80-133">-SnapshotId</span></span>
<span data-ttu-id="85d80-134">SnapshotId migawki.</span><span class="sxs-lookup"><span data-stu-id="85d80-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="85d80-135">Identyfikator UUID (wersja 4) służący do identyfikowania migawki</span><span class="sxs-lookup"><span data-stu-id="85d80-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d80-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85d80-136">-Confirm</span></span>
<span data-ttu-id="85d80-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85d80-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85d80-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85d80-138">-WhatIf</span></span>
<span data-ttu-id="85d80-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85d80-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85d80-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85d80-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85d80-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d80-141">CommonParameters</span></span>
<span data-ttu-id="85d80-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d80-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d80-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d80-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d80-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85d80-144">INPUTS</span></span>

### <span data-ttu-id="85d80-145">System. String</span><span class="sxs-lookup"><span data-stu-id="85d80-145">System.String</span></span>

### <span data-ttu-id="85d80-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="85d80-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="85d80-147">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="85d80-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="85d80-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85d80-148">OUTPUTS</span></span>

### <span data-ttu-id="85d80-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85d80-149">System.Boolean</span></span>

## <span data-ttu-id="85d80-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85d80-150">NOTES</span></span>

## <span data-ttu-id="85d80-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85d80-151">RELATED LINKS</span></span>
