---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489981"
---
# <span data-ttu-id="1b376-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1b376-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="1b376-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b376-102">SYNOPSIS</span></span>
<span data-ttu-id="1b376-103">Tworzy nową pulę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="1b376-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="1b376-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b376-104">SYNTAX</span></span>

### <span data-ttu-id="1b376-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1b376-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b376-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b376-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b376-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b376-107">DESCRIPTION</span></span>
<span data-ttu-id="1b376-108">Polecenie cmdlet **New-AzNetAppFilesPool** tworzy pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="1b376-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="1b376-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b376-109">EXAMPLES</span></span>

### <span data-ttu-id="1b376-110">Przykład 1. Tworzenie puli ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="1b376-111">To polecenie tworzy nową pulę ANF "MyAnfPool" w ramach konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="1b376-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="1b376-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b376-112">PARAMETERS</span></span>

### <span data-ttu-id="1b376-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b376-113">-AccountName</span></span>
<span data-ttu-id="1b376-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1b376-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="1b376-115">-AccountObject</span></span>
<span data-ttu-id="1b376-116">Konto nowego obiektu puli</span><span class="sxs-lookup"><span data-stu-id="1b376-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="1b376-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b376-117">-DefaultProfile</span></span>
<span data-ttu-id="1b376-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b376-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b376-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b376-119">-Location</span></span>
<span data-ttu-id="1b376-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="1b376-120">The location of the resource</span></span>

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

### <span data-ttu-id="1b376-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b376-121">-Name</span></span>
<span data-ttu-id="1b376-122">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1b376-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="1b376-123">-PoolSize</span></span>
<span data-ttu-id="1b376-124">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="1b376-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="1b376-125">-QosType</span></span>
<span data-ttu-id="1b376-126">Typ QoS puli.</span><span class="sxs-lookup"><span data-stu-id="1b376-126">The qos type of the pool.</span></span> <span data-ttu-id="1b376-127">Możliwe wartości to: "Auto", "ręczna".</span><span class="sxs-lookup"><span data-stu-id="1b376-127">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="1b376-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b376-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b376-129">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1b376-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="1b376-130">-ServiceLevel</span></span>
<span data-ttu-id="1b376-131">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="1b376-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="1b376-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b376-132">-Tag</span></span>
<span data-ttu-id="1b376-133">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="1b376-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1b376-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b376-134">-Confirm</span></span>
<span data-ttu-id="1b376-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b376-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b376-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b376-136">-WhatIf</span></span>
<span data-ttu-id="1b376-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b376-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b376-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b376-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b376-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b376-139">CommonParameters</span></span>
<span data-ttu-id="1b376-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b376-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b376-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b376-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b376-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b376-142">INPUTS</span></span>

### <span data-ttu-id="1b376-143">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1b376-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1b376-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b376-144">OUTPUTS</span></span>

### <span data-ttu-id="1b376-145">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1b376-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1b376-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b376-146">NOTES</span></span>

## <span data-ttu-id="1b376-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b376-147">RELATED LINKS</span></span>
