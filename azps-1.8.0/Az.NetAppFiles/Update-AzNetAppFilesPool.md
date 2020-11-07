---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709725"
---
# <span data-ttu-id="275c8-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="275c8-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="275c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="275c8-102">SYNOPSIS</span></span>
<span data-ttu-id="275c8-103">Umożliwia zaktualizowanie puli plików usługi Azure NetApp (ANF) przy użyciu nowego zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="275c8-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="275c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="275c8-104">SYNTAX</span></span>

### <span data-ttu-id="275c8-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="275c8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="275c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275c8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="275c8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275c8-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="275c8-108">DESCRIPTION</span></span>
<span data-ttu-id="275c8-109">Polecenie cmdlet **Update-AzNetAppFilesPool** modyfikuje pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="275c8-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="275c8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="275c8-110">EXAMPLES</span></span>

### <span data-ttu-id="275c8-111">Przykład 1. Modyfikowanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="275c8-112">To polecenie powoduje zmianę puli ANF "MyAnfPool" w celu uzyskania określonego rozmiaru i poziomu.</span><span class="sxs-lookup"><span data-stu-id="275c8-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="275c8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="275c8-113">PARAMETERS</span></span>

### <span data-ttu-id="275c8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="275c8-114">-AccountName</span></span>
<span data-ttu-id="275c8-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="275c8-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="275c8-116">-AccountObject</span></span>
<span data-ttu-id="275c8-117">Obiekt konta zawierający pulę do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="275c8-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="275c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275c8-118">-DefaultProfile</span></span>
<span data-ttu-id="275c8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="275c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275c8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="275c8-120">-InputObject</span></span>
<span data-ttu-id="275c8-121">Obiekt puli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="275c8-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="275c8-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="275c8-122">-Location</span></span>
<span data-ttu-id="275c8-123">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="275c8-123">The location of the resource</span></span>

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

### <span data-ttu-id="275c8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="275c8-124">-Name</span></span>
<span data-ttu-id="275c8-125">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275c8-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="275c8-126">-PoolSize</span></span>
<span data-ttu-id="275c8-127">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-127">The size of the ANF pool</span></span>

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

### <span data-ttu-id="275c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="275c8-129">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="275c8-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="275c8-130">-ServiceLevel</span></span>
<span data-ttu-id="275c8-131">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="275c8-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="275c8-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="275c8-132">-Confirm</span></span>
<span data-ttu-id="275c8-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275c8-134">-WhatIf</span></span>
<span data-ttu-id="275c8-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275c8-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="275c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275c8-137">CommonParameters</span></span>
<span data-ttu-id="275c8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="275c8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275c8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275c8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275c8-140">INPUTS</span></span>

### <span data-ttu-id="275c8-141">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="275c8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="275c8-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="275c8-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="275c8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="275c8-143">OUTPUTS</span></span>

### <span data-ttu-id="275c8-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="275c8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="275c8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="275c8-145">NOTES</span></span>

## <span data-ttu-id="275c8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275c8-146">RELATED LINKS</span></span>
