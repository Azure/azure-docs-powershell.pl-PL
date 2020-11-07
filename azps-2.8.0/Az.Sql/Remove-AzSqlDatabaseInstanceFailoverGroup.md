---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887346"
---
# <span data-ttu-id="b42ca-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b42ca-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="b42ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b42ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b42ca-103">Usuwa grupę wystąpień awaryjnych.</span><span class="sxs-lookup"><span data-stu-id="b42ca-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="b42ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b42ca-104">SYNTAX</span></span>

### <span data-ttu-id="b42ca-105">RemoveIFGDefault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b42ca-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b42ca-106">Usuwanie grupy trybu failover wystąpienia z identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="b42ca-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b42ca-107">Usuwanie grupy wystąpień awaryjnych z definicji wystąpienia AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b42ca-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b42ca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b42ca-108">DESCRIPTION</span></span>
<span data-ttu-id="b42ca-109">To polecenie usuwa grupę awaryjną wystąpienia o określonej nazwie, pozostawiając wszystkie bazy danych nienaruszone.</span><span class="sxs-lookup"><span data-stu-id="b42ca-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="b42ca-110">Punkt końcowy odbiornika zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="b42ca-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="b42ca-111">Aby wykonać polecenie, należy użyć głównego regionu grupy tryb failover.</span><span class="sxs-lookup"><span data-stu-id="b42ca-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="b42ca-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b42ca-112">EXAMPLES</span></span>

### <span data-ttu-id="b42ca-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b42ca-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="b42ca-114">Usuwanie grupy wystąpień awaryjnych.</span><span class="sxs-lookup"><span data-stu-id="b42ca-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="b42ca-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b42ca-115">PARAMETERS</span></span>

### <span data-ttu-id="b42ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42ca-116">-DefaultProfile</span></span>
<span data-ttu-id="b42ca-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b42ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b42ca-118">-Force</span></span>
<span data-ttu-id="b42ca-119">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="b42ca-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b42ca-120">-InputObject</span></span>
<span data-ttu-id="b42ca-121">Obiekt grupy trybu failover wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="b42ca-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b42ca-122">-Location</span></span>
<span data-ttu-id="b42ca-123">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="b42ca-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b42ca-124">-Name</span></span>
<span data-ttu-id="b42ca-125">Nazwa grupy tryb failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b42ca-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b42ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="b42ca-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b42ca-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b42ca-128">-ResourceId</span></span>
<span data-ttu-id="b42ca-129">Identyfikator zasobu grupy trybu failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b42ca-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b42ca-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b42ca-130">-Confirm</span></span>
<span data-ttu-id="b42ca-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b42ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b42ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b42ca-132">-WhatIf</span></span>
<span data-ttu-id="b42ca-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b42ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b42ca-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b42ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b42ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42ca-135">CommonParameters</span></span>
<span data-ttu-id="b42ca-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b42ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42ca-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b42ca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42ca-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b42ca-138">INPUTS</span></span>

### <span data-ttu-id="b42ca-139">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b42ca-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="b42ca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b42ca-140">System.String</span></span>

## <span data-ttu-id="b42ca-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b42ca-141">OUTPUTS</span></span>

### <span data-ttu-id="b42ca-142">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b42ca-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="b42ca-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b42ca-143">NOTES</span></span>

## <span data-ttu-id="b42ca-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b42ca-144">RELATED LINKS</span></span>
