---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341398"
---
# <span data-ttu-id="7e428-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="7e428-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="7e428-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e428-102">SYNOPSIS</span></span>
<span data-ttu-id="7e428-103">Zawieszanie/Przerywanie połączenia replikacji na woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="7e428-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="7e428-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e428-104">SYNTAX</span></span>

### <span data-ttu-id="7e428-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e428-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e428-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e428-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e428-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e428-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e428-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e428-108">DESCRIPTION</span></span>
<span data-ttu-id="7e428-109">Zawieszanie/Przerywanie połączenia replikacji na woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="7e428-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="7e428-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e428-110">EXAMPLES</span></span>

### <span data-ttu-id="7e428-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e428-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="7e428-112">To polecenie zawiesza połączenie replikacji ANF w woluminie "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="7e428-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="7e428-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e428-113">PARAMETERS</span></span>

### <span data-ttu-id="7e428-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e428-114">-AccountName</span></span>
<span data-ttu-id="7e428-115">Nazwa konta ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="7e428-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="7e428-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e428-116">-DefaultProfile</span></span>
<span data-ttu-id="7e428-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e428-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e428-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="7e428-118">-ForceBreak</span></span>
<span data-ttu-id="7e428-119">Jeśli replikacja jest w stanie transferowania i chcesz wymusić zerwanie replikacji, ustaw wartość PRAWDA</span><span class="sxs-lookup"><span data-stu-id="7e428-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e428-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e428-120">-InputObject</span></span>
<span data-ttu-id="7e428-121">Obiekt woluminu docelowego ANF z replikacją do podziału</span><span class="sxs-lookup"><span data-stu-id="7e428-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="7e428-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e428-122">-Name</span></span>
<span data-ttu-id="7e428-123">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="7e428-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7e428-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e428-124">-PassThru</span></span>
<span data-ttu-id="7e428-125">Zwraca, czy przerwano wykonywanie replikacji woluminu.</span><span class="sxs-lookup"><span data-stu-id="7e428-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="7e428-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7e428-126">-PoolName</span></span>
<span data-ttu-id="7e428-127">Nazwa puli ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="7e428-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="7e428-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e428-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e428-129">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="7e428-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7e428-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e428-130">-ResourceId</span></span>
<span data-ttu-id="7e428-131">Identyfikator zasobu w docelowym woluminie replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="7e428-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7e428-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e428-132">-Confirm</span></span>
<span data-ttu-id="7e428-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e428-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e428-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e428-134">-WhatIf</span></span>
<span data-ttu-id="7e428-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e428-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e428-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e428-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e428-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e428-137">CommonParameters</span></span>
<span data-ttu-id="7e428-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e428-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e428-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e428-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e428-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e428-140">INPUTS</span></span>

### <span data-ttu-id="7e428-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e428-141">System.String</span></span>

### <span data-ttu-id="7e428-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7e428-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7e428-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e428-143">OUTPUTS</span></span>

### <span data-ttu-id="7e428-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e428-144">System.Boolean</span></span>

## <span data-ttu-id="7e428-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e428-145">NOTES</span></span>

## <span data-ttu-id="7e428-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e428-146">RELATED LINKS</span></span>
