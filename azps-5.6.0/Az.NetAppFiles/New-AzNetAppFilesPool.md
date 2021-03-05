---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 30a569c16a2f3da135f77061e8ff5373c45b2598
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968449"
---
# <span data-ttu-id="03fc2-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="03fc2-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="03fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="03fc2-103">Tworzy nową pulę plików AZURE NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="03fc2-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="03fc2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03fc2-104">SYNTAX</span></span>

### <span data-ttu-id="03fc2-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="03fc2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03fc2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fc2-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03fc2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03fc2-107">DESCRIPTION</span></span>
<span data-ttu-id="03fc2-108">Polecenie **cmdlet New-AzNetAppFilesPool** tworzy pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="03fc2-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="03fc2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03fc2-109">EXAMPLES</span></span>

### <span data-ttu-id="03fc2-110">Przykład 1. Tworzenie puli anfów</span><span class="sxs-lookup"><span data-stu-id="03fc2-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="03fc2-111">To polecenie tworzy nową pulę ANF "MyAnfPool" w ramach konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="03fc2-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="03fc2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03fc2-112">PARAMETERS</span></span>

### <span data-ttu-id="03fc2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03fc2-113">-AccountName</span></span>
<span data-ttu-id="03fc2-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="03fc2-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="03fc2-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="03fc2-115">-AccountObject</span></span>
<span data-ttu-id="03fc2-116">Konto nowego obiektu puli</span><span class="sxs-lookup"><span data-stu-id="03fc2-116">The account for the new pool object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03fc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fc2-117">-DefaultProfile</span></span>
<span data-ttu-id="03fc2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03fc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fc2-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03fc2-119">-Location</span></span>
<span data-ttu-id="03fc2-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="03fc2-120">The location of the resource</span></span>

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

### <span data-ttu-id="03fc2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03fc2-121">-Name</span></span>
<span data-ttu-id="03fc2-122">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="03fc2-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc2-123">- PoolSize</span><span class="sxs-lookup"><span data-stu-id="03fc2-123">-PoolSize</span></span>
<span data-ttu-id="03fc2-124">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="03fc2-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc2-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="03fc2-125">-QosType</span></span>
<span data-ttu-id="03fc2-126">Typ puli qos.</span><span class="sxs-lookup"><span data-stu-id="03fc2-126">The qos type of the pool.</span></span> <span data-ttu-id="03fc2-127">Możliwe wartości: "Automatycznie", "Ręcznie"</span><span class="sxs-lookup"><span data-stu-id="03fc2-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fc2-128">-ResourceGroupName</span></span>
<span data-ttu-id="03fc2-129">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="03fc2-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="03fc2-130">- ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="03fc2-130">-ServiceLevel</span></span>
<span data-ttu-id="03fc2-131">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="03fc2-131">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc2-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="03fc2-132">-Tag</span></span>
<span data-ttu-id="03fc2-133">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="03fc2-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="03fc2-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03fc2-134">-Confirm</span></span>
<span data-ttu-id="03fc2-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03fc2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fc2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fc2-136">-WhatIf</span></span>
<span data-ttu-id="03fc2-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03fc2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fc2-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03fc2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fc2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fc2-139">CommonParameters</span></span>
<span data-ttu-id="03fc2-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fc2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fc2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03fc2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fc2-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03fc2-142">INPUTS</span></span>

### <span data-ttu-id="03fc2-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="03fc2-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="03fc2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03fc2-144">OUTPUTS</span></span>

### <span data-ttu-id="03fc2-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="03fc2-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="03fc2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03fc2-146">NOTES</span></span>

## <span data-ttu-id="03fc2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03fc2-147">RELATED LINKS</span></span>
