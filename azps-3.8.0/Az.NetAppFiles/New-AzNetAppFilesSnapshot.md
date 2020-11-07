---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47383ee57d527f6348781e57ed965e1ed8d36ef2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894210"
---
# <span data-ttu-id="26f84-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="26f84-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="26f84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26f84-102">SYNOPSIS</span></span>
<span data-ttu-id="26f84-103">Tworzy nową migawkę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="26f84-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="26f84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26f84-104">SYNTAX</span></span>

### <span data-ttu-id="26f84-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26f84-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f84-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f84-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f84-107">Opis</span><span class="sxs-lookup"><span data-stu-id="26f84-107">DESCRIPTION</span></span>
<span data-ttu-id="26f84-108">Polecenie cmdlet **New-AzNetAppFilesSnapshot** umożliwia utworzenie migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="26f84-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="26f84-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26f84-109">EXAMPLES</span></span>

### <span data-ttu-id="26f84-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26f84-110">Example 1</span></span>
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

<span data-ttu-id="26f84-111">To polecenie tworzy nową migawkę ANF "MyAnfSnapshot" w woluminie "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="26f84-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="26f84-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26f84-112">PARAMETERS</span></span>

### <span data-ttu-id="26f84-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26f84-113">-AccountName</span></span>
<span data-ttu-id="26f84-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="26f84-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="26f84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f84-115">-DefaultProfile</span></span>
<span data-ttu-id="26f84-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26f84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f84-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="26f84-117">-FileSystemId</span></span>
<span data-ttu-id="26f84-118">Identyfikator systemu plików</span><span class="sxs-lookup"><span data-stu-id="26f84-118">The file system id</span></span>

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

### <span data-ttu-id="26f84-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26f84-119">-Location</span></span>
<span data-ttu-id="26f84-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="26f84-120">The location of the resource</span></span>

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

### <span data-ttu-id="26f84-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26f84-121">-Name</span></span>
<span data-ttu-id="26f84-122">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="26f84-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f84-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="26f84-123">-PoolName</span></span>
<span data-ttu-id="26f84-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="26f84-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="26f84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f84-125">-ResourceGroupName</span></span>
<span data-ttu-id="26f84-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="26f84-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="26f84-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="26f84-127">-Tag</span></span>
<span data-ttu-id="26f84-128">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="26f84-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="26f84-129">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="26f84-129">-VolumeName</span></span>
<span data-ttu-id="26f84-130">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="26f84-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="26f84-131">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="26f84-131">-VolumeObject</span></span>
<span data-ttu-id="26f84-132">Głośność nowego obiektu migawki</span><span class="sxs-lookup"><span data-stu-id="26f84-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26f84-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26f84-133">-Confirm</span></span>
<span data-ttu-id="26f84-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26f84-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f84-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f84-135">-WhatIf</span></span>
<span data-ttu-id="26f84-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26f84-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f84-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26f84-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f84-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f84-138">CommonParameters</span></span>
<span data-ttu-id="26f84-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f84-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26f84-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f84-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f84-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26f84-141">INPUTS</span></span>

### <span data-ttu-id="26f84-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="26f84-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="26f84-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26f84-143">OUTPUTS</span></span>

### <span data-ttu-id="26f84-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="26f84-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="26f84-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26f84-145">NOTES</span></span>

## <span data-ttu-id="26f84-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26f84-146">RELATED LINKS</span></span>
