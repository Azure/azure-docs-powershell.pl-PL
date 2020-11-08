---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064005"
---
# <span data-ttu-id="054cb-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="054cb-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="054cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="054cb-102">SYNOPSIS</span></span>
<span data-ttu-id="054cb-103">Umożliwia zaktualizowanie puli plików usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="054cb-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="054cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="054cb-104">SYNTAX</span></span>

### <span data-ttu-id="054cb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="054cb-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="054cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="054cb-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="054cb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="054cb-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="054cb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="054cb-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="054cb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="054cb-109">DESCRIPTION</span></span>
<span data-ttu-id="054cb-110">Polecenie cmdlet **Update-AzNetAppFilesPool** modyfikuje pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="054cb-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="054cb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="054cb-111">EXAMPLES</span></span>

### <span data-ttu-id="054cb-112">Przykład 1. Modyfikowanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="054cb-113">To polecenie powoduje zmianę puli ANF "MyAnfPool" w celu uzyskania określonego rozmiaru i poziomu.</span><span class="sxs-lookup"><span data-stu-id="054cb-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="054cb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="054cb-114">PARAMETERS</span></span>

### <span data-ttu-id="054cb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="054cb-115">-AccountName</span></span>
<span data-ttu-id="054cb-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="054cb-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="054cb-117">-AccountObject</span></span>
<span data-ttu-id="054cb-118">Obiekt konta zawierający pulę do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="054cb-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="054cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054cb-119">-DefaultProfile</span></span>
<span data-ttu-id="054cb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="054cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="054cb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="054cb-121">-InputObject</span></span>
<span data-ttu-id="054cb-122">Obiekt puli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="054cb-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="054cb-123">-Location</span></span>
<span data-ttu-id="054cb-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="054cb-124">The location of the resource</span></span>

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

### <span data-ttu-id="054cb-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="054cb-125">-Name</span></span>
<span data-ttu-id="054cb-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="054cb-127">-PoolSize</span></span>
<span data-ttu-id="054cb-128">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="054cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="054cb-130">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="054cb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="054cb-131">-ResourceId</span></span>
<span data-ttu-id="054cb-132">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="054cb-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="054cb-133">-ServiceLevel</span></span>
<span data-ttu-id="054cb-134">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="054cb-134">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="054cb-135">-Tag</span></span>
<span data-ttu-id="054cb-136">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="054cb-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="054cb-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="054cb-137">-Confirm</span></span>
<span data-ttu-id="054cb-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="054cb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="054cb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="054cb-139">-WhatIf</span></span>
<span data-ttu-id="054cb-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="054cb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="054cb-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="054cb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="054cb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054cb-142">CommonParameters</span></span>
<span data-ttu-id="054cb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="054cb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054cb-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="054cb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054cb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="054cb-145">INPUTS</span></span>

### <span data-ttu-id="054cb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="054cb-146">System.String</span></span>

### <span data-ttu-id="054cb-147">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="054cb-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="054cb-148">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="054cb-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="054cb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="054cb-149">OUTPUTS</span></span>

### <span data-ttu-id="054cb-150">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="054cb-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="054cb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="054cb-151">NOTES</span></span>

## <span data-ttu-id="054cb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="054cb-152">RELATED LINKS</span></span>
