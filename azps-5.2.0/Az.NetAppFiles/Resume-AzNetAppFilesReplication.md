---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354337"
---
# <span data-ttu-id="1a932-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="1a932-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="1a932-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a932-102">SYNOPSIS</span></span>
<span data-ttu-id="1a932-103">Wznów lub ponownie zsynchronizuj połączenie na woluminie docelowym.</span><span class="sxs-lookup"><span data-stu-id="1a932-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="1a932-104">Jeśli operacja zostanie uruchomiona na woluminie źródłowym, ponowne zsynchronizowanie połączenia i zsynchronizowanie z lokalizacji źródłowej z miejscem docelowym.</span><span class="sxs-lookup"><span data-stu-id="1a932-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="1a932-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a932-105">SYNTAX</span></span>

### <span data-ttu-id="1a932-106">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a932-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a932-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a932-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a932-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a932-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a932-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1a932-109">DESCRIPTION</span></span>
<span data-ttu-id="1a932-110">Wznów lub ponownie zsynchronizuj połączenie na woluminie docelowym</span><span class="sxs-lookup"><span data-stu-id="1a932-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="1a932-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a932-111">EXAMPLES</span></span>

### <span data-ttu-id="1a932-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a932-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="1a932-113">To polecenie wznawia połączenie replikacji ANF w woluminie "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="1a932-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="1a932-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a932-114">PARAMETERS</span></span>

### <span data-ttu-id="1a932-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a932-115">-AccountName</span></span>
<span data-ttu-id="1a932-116">Nazwa konta ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1a932-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="1a932-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a932-117">-DefaultProfile</span></span>
<span data-ttu-id="1a932-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a932-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a932-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a932-119">-InputObject</span></span>
<span data-ttu-id="1a932-120">Obiekt woluminu docelowego replikacji ANF do ponownej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1a932-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="1a932-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a932-121">-Name</span></span>
<span data-ttu-id="1a932-122">Nazwa woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1a932-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1a932-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a932-123">-PassThru</span></span>
<span data-ttu-id="1a932-124">Zwraca, czy została wykonana ponowna synchronizacja określonego woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1a932-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="1a932-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1a932-125">-PoolName</span></span>
<span data-ttu-id="1a932-126">Nazwa puli ANF woluminu replikacji</span><span class="sxs-lookup"><span data-stu-id="1a932-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="1a932-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a932-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a932-128">Grupa zasobów woluminu docelowego replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1a932-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1a932-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a932-129">-ResourceId</span></span>
<span data-ttu-id="1a932-130">Identyfikator zasobu w docelowym woluminie replikacji ANF</span><span class="sxs-lookup"><span data-stu-id="1a932-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1a932-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a932-131">-Confirm</span></span>
<span data-ttu-id="1a932-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a932-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a932-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a932-133">-WhatIf</span></span>
<span data-ttu-id="1a932-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a932-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a932-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a932-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a932-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a932-136">CommonParameters</span></span>
<span data-ttu-id="1a932-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a932-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a932-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a932-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a932-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a932-139">INPUTS</span></span>

### <span data-ttu-id="1a932-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1a932-140">System.String</span></span>

### <span data-ttu-id="1a932-141">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1a932-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1a932-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a932-142">OUTPUTS</span></span>

### <span data-ttu-id="1a932-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a932-143">System.Boolean</span></span>

## <span data-ttu-id="1a932-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a932-144">NOTES</span></span>

## <span data-ttu-id="1a932-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a932-145">RELATED LINKS</span></span>
