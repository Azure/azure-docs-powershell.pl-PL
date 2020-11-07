---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2214e84f4dd18981a8588ea32978a43e6d6e8045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894197"
---
# <span data-ttu-id="1787b-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1787b-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="1787b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1787b-102">SYNOPSIS</span></span>
<span data-ttu-id="1787b-103">Tworzy nowy wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="1787b-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="1787b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1787b-104">SYNTAX</span></span>

### <span data-ttu-id="1787b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1787b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1787b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1787b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1787b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1787b-107">DESCRIPTION</span></span>
<span data-ttu-id="1787b-108">Polecenie cmdlet **New-AzNetAppFilesVolume** tworzy wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="1787b-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="1787b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1787b-109">EXAMPLES</span></span>

### <span data-ttu-id="1787b-110">Przykład 1. Tworzenie woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="1787b-111">To polecenie tworzy nowy wolumin ANF "MyAnfVolume" w puli "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="1787b-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="1787b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1787b-112">PARAMETERS</span></span>

### <span data-ttu-id="1787b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1787b-113">-AccountName</span></span>
<span data-ttu-id="1787b-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1787b-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="1787b-115">-CreationToken</span></span>
<span data-ttu-id="1787b-116">Unikatowa ścieżka pliku dla woluminu</span><span class="sxs-lookup"><span data-stu-id="1787b-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="1787b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1787b-117">-DefaultProfile</span></span>
<span data-ttu-id="1787b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1787b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1787b-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="1787b-119">-ExportPolicy</span></span>
<span data-ttu-id="1787b-120">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="1787b-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1787b-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1787b-121">-Location</span></span>
<span data-ttu-id="1787b-122">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="1787b-122">The location of the resource</span></span>

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

### <span data-ttu-id="1787b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1787b-123">-Name</span></span>
<span data-ttu-id="1787b-124">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="1787b-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1787b-125">-PoolName</span></span>
<span data-ttu-id="1787b-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1787b-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="1787b-127">-PoolObject</span></span>
<span data-ttu-id="1787b-128">Pula dla nowego obiektu woluminu</span><span class="sxs-lookup"><span data-stu-id="1787b-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="1787b-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="1787b-129">-ProtocolType</span></span>
<span data-ttu-id="1787b-130">Tablica Hashtable, która reprezentuje zasady eksportu</span><span class="sxs-lookup"><span data-stu-id="1787b-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1787b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1787b-131">-ResourceGroupName</span></span>
<span data-ttu-id="1787b-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1787b-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="1787b-133">-ServiceLevel</span></span>
<span data-ttu-id="1787b-134">Poziom usługi woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="1787b-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1787b-135">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1787b-135">-SubnetId</span></span>
<span data-ttu-id="1787b-136">Identyfikator URI zasobu platformy Azure dla delegowanej podsieci</span><span class="sxs-lookup"><span data-stu-id="1787b-136">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="1787b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="1787b-137">-Tag</span></span>
<span data-ttu-id="1787b-138">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="1787b-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1787b-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="1787b-139">-UsageThreshold</span></span>
<span data-ttu-id="1787b-140">Maksymalny przydział przestrzeni dyskowej dozwolony dla systemu plików w bajtach</span><span class="sxs-lookup"><span data-stu-id="1787b-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="1787b-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1787b-141">-Confirm</span></span>
<span data-ttu-id="1787b-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1787b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1787b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1787b-143">-WhatIf</span></span>
<span data-ttu-id="1787b-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1787b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1787b-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1787b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1787b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1787b-146">CommonParameters</span></span>
<span data-ttu-id="1787b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1787b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1787b-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1787b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1787b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1787b-149">INPUTS</span></span>

### <span data-ttu-id="1787b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1787b-150">System.String</span></span>

### <span data-ttu-id="1787b-151">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1787b-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1787b-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1787b-152">OUTPUTS</span></span>

### <span data-ttu-id="1787b-153">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1787b-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1787b-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1787b-154">NOTES</span></span>

## <span data-ttu-id="1787b-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1787b-155">RELATED LINKS</span></span>
