---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232864"
---
# <span data-ttu-id="20b34-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="20b34-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="20b34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20b34-102">SYNOPSIS</span></span>
<span data-ttu-id="20b34-103">Tworzy nową migawkę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="20b34-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="20b34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20b34-104">SYNTAX</span></span>

### <span data-ttu-id="20b34-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20b34-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b34-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20b34-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b34-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20b34-107">DESCRIPTION</span></span>
<span data-ttu-id="20b34-108">Polecenie cmdlet **New-AzNetAppFilesSnapshot** umożliwia utworzenie migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="20b34-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="20b34-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20b34-109">EXAMPLES</span></span>

### <span data-ttu-id="20b34-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20b34-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="20b34-111">To polecenie tworzy nową migawkę ANF "MyAnfSnapshot" w woluminie "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="20b34-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="20b34-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20b34-112">PARAMETERS</span></span>

### <span data-ttu-id="20b34-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20b34-113">-AccountName</span></span>
<span data-ttu-id="20b34-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="20b34-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="20b34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b34-115">-DefaultProfile</span></span>
<span data-ttu-id="20b34-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20b34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b34-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="20b34-117">-FileSystemId</span></span>
<span data-ttu-id="20b34-118">Identyfikator systemu plików</span><span class="sxs-lookup"><span data-stu-id="20b34-118">The file system id</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b34-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="20b34-119">-Location</span></span>
<span data-ttu-id="20b34-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="20b34-120">The location of the resource</span></span>

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

### <span data-ttu-id="20b34-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20b34-121">-Name</span></span>
<span data-ttu-id="20b34-122">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="20b34-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b34-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="20b34-123">-PoolName</span></span>
<span data-ttu-id="20b34-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="20b34-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="20b34-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b34-125">-ResourceGroupName</span></span>
<span data-ttu-id="20b34-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="20b34-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="20b34-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="20b34-127">-Tag</span></span>
<span data-ttu-id="20b34-128">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="20b34-128">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b34-129">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="20b34-129">-VolumeName</span></span>
<span data-ttu-id="20b34-130">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="20b34-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="20b34-131">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="20b34-131">-VolumeObject</span></span>
<span data-ttu-id="20b34-132">Głośność nowego obiektu migawki</span><span class="sxs-lookup"><span data-stu-id="20b34-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="20b34-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20b34-133">-Confirm</span></span>
<span data-ttu-id="20b34-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b34-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b34-135">-WhatIf</span></span>
<span data-ttu-id="20b34-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b34-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b34-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20b34-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b34-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b34-138">CommonParameters</span></span>
<span data-ttu-id="20b34-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b34-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b34-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20b34-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b34-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20b34-141">INPUTS</span></span>

### <span data-ttu-id="20b34-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="20b34-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="20b34-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20b34-143">OUTPUTS</span></span>

### <span data-ttu-id="20b34-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="20b34-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="20b34-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20b34-145">NOTES</span></span>

## <span data-ttu-id="20b34-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20b34-146">RELATED LINKS</span></span>
