---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318631"
---
# <span data-ttu-id="e6f7e-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="e6f7e-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="e6f7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f7e-103">Zawieszanie/Przerywanie połączenia replikacji na woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="e6f7e-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e6f7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6f7e-104">SYNTAX</span></span>

### <span data-ttu-id="e6f7e-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6f7e-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f7e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f7e-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f7e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f7e-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f7e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e6f7e-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f7e-109">Zawieszanie/Przerywanie połączenia replikacji na woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="e6f7e-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e6f7e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6f7e-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f7e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6f7e-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="e6f7e-112">To polecenie zawiesza połączenie replikacji ANF w woluminie "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="e6f7e-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="e6f7e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6f7e-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f7e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e6f7e-114">-AccountName</span></span>
<span data-ttu-id="e6f7e-115">Nazwa konta ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="e6f7e-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="e6f7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f7e-116">-DefaultProfile</span></span>
<span data-ttu-id="e6f7e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f7e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6f7e-118">-InputObject</span></span>
<span data-ttu-id="e6f7e-119">Obiekt woluminu docelowego ANF z replikacją do podziału</span><span class="sxs-lookup"><span data-stu-id="e6f7e-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="e6f7e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6f7e-120">-Name</span></span>
<span data-ttu-id="e6f7e-121">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="e6f7e-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e6f7e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f7e-122">-PassThru</span></span>
<span data-ttu-id="e6f7e-123">Zwraca, czy przerwano wykonywanie replikacji woluminu.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="e6f7e-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e6f7e-124">-PoolName</span></span>
<span data-ttu-id="e6f7e-125">Nazwa puli ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="e6f7e-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="e6f7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6f7e-127">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="e6f7e-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e6f7e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f7e-128">-ResourceId</span></span>
<span data-ttu-id="e6f7e-129">Identyfikator zasobu w docelowym woluminie replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="e6f7e-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e6f7e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6f7e-130">-Confirm</span></span>
<span data-ttu-id="e6f7e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f7e-132">-WhatIf</span></span>
<span data-ttu-id="e6f7e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f7e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f7e-135">CommonParameters</span></span>
<span data-ttu-id="e6f7e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f7e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6f7e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f7e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6f7e-138">INPUTS</span></span>

### <span data-ttu-id="e6f7e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f7e-139">System.String</span></span>

### <span data-ttu-id="e6f7e-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e6f7e-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e6f7e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6f7e-141">OUTPUTS</span></span>

### <span data-ttu-id="e6f7e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6f7e-142">System.Boolean</span></span>

## <span data-ttu-id="e6f7e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6f7e-143">NOTES</span></span>

## <span data-ttu-id="e6f7e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6f7e-144">RELATED LINKS</span></span>
