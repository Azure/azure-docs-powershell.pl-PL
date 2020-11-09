---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318649"
---
# <span data-ttu-id="a607a-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="a607a-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="a607a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a607a-102">SYNOPSIS</span></span>
<span data-ttu-id="a607a-103">Usuwanie lub usuwanie połączenia replikacji na woluminie docelowym oraz wysyłanie wersji do replikacji źródłowej</span><span class="sxs-lookup"><span data-stu-id="a607a-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="a607a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a607a-104">SYNTAX</span></span>

### <span data-ttu-id="a607a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a607a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a607a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a607a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a607a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a607a-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a607a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a607a-108">DESCRIPTION</span></span>
<span data-ttu-id="a607a-109">Usuwanie lub usuwanie połączenia replikacji na woluminie docelowym oraz wysyłanie wersji do replikacji źródłowej</span><span class="sxs-lookup"><span data-stu-id="a607a-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="a607a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a607a-110">EXAMPLES</span></span>

### <span data-ttu-id="a607a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a607a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="a607a-112">To polecenie usuwa połączenie replikacji ANF w woluminie "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="a607a-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="a607a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a607a-113">PARAMETERS</span></span>

### <span data-ttu-id="a607a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a607a-114">-AccountName</span></span>
<span data-ttu-id="a607a-115">Nazwa konta ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="a607a-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="a607a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a607a-116">-DefaultProfile</span></span>
<span data-ttu-id="a607a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a607a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a607a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a607a-118">-InputObject</span></span>
<span data-ttu-id="a607a-119">Wolumin docelowy ANF z replikacją do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a607a-119">The ANF destination volume with the replication to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a607a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a607a-120">-Name</span></span>
<span data-ttu-id="a607a-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="a607a-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a607a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a607a-122">-PassThru</span></span>
<span data-ttu-id="a607a-123">Zwraca, czy określona replikacja ANF została pomyślnie usunięta.</span><span class="sxs-lookup"><span data-stu-id="a607a-123">Return whether the specified ANF replication was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a607a-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a607a-124">-PoolName</span></span>
<span data-ttu-id="a607a-125">Nazwa puli ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="a607a-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="a607a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a607a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a607a-127">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="a607a-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a607a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a607a-128">-ResourceId</span></span>
<span data-ttu-id="a607a-129">Identyfikator zasobu w docelowym woluminie replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="a607a-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a607a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a607a-130">-Confirm</span></span>
<span data-ttu-id="a607a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a607a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a607a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a607a-132">-WhatIf</span></span>
<span data-ttu-id="a607a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a607a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a607a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a607a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a607a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a607a-135">CommonParameters</span></span>
<span data-ttu-id="a607a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a607a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a607a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a607a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a607a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a607a-138">INPUTS</span></span>

### <span data-ttu-id="a607a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a607a-139">System.String</span></span>

### <span data-ttu-id="a607a-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a607a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a607a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a607a-141">OUTPUTS</span></span>

### <span data-ttu-id="a607a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a607a-142">System.Boolean</span></span>

## <span data-ttu-id="a607a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a607a-143">NOTES</span></span>

## <span data-ttu-id="a607a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a607a-144">RELATED LINKS</span></span>
