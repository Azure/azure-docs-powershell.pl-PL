---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234263"
---
# <span data-ttu-id="bd0e0-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bd0e0-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="bd0e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0e0-103">Usuwa wystąpienie bazy danych zarządzanej przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="bd0e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd0e0-104">SYNTAX</span></span>

### <span data-ttu-id="bd0e0-105">RemoveInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd0e0-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd0e0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="bd0e0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd0e0-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="bd0e0-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bd0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="bd0e0-109">Polecenie cmdlet **Remove-AzSqlInstance** umożliwia usunięcie wystąpienia zarządzanego bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="bd0e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="bd0e0-111">Przykład 1: usuwanie wystąpienia</span><span class="sxs-lookup"><span data-stu-id="bd0e0-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bd0e0-112">To polecenie powoduje usunięcie wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="bd0e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd0e0-113">PARAMETERS</span></span>

### <span data-ttu-id="bd0e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0e0-114">-DefaultProfile</span></span>
<span data-ttu-id="bd0e0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0e0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bd0e0-116">-Force</span></span>
<span data-ttu-id="bd0e0-117">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="bd0e0-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bd0e0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd0e0-118">-InputObject</span></span>
<span data-ttu-id="bd0e0-119">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="bd0e0-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0e0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd0e0-120">-Name</span></span>
<span data-ttu-id="bd0e0-121">Nazwa wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd0e0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd0e0-124">-ResourceId</span></span>
<span data-ttu-id="bd0e0-125">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="bd0e0-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0e0-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd0e0-126">-Confirm</span></span>
<span data-ttu-id="bd0e0-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd0e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0e0-128">-WhatIf</span></span>
<span data-ttu-id="bd0e0-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd0e0-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd0e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0e0-131">CommonParameters</span></span>
<span data-ttu-id="bd0e0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0e0-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd0e0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0e0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd0e0-134">INPUTS</span></span>

### <span data-ttu-id="bd0e0-135">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="bd0e0-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="bd0e0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0e0-136">System.String</span></span>

## <span data-ttu-id="bd0e0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd0e0-137">OUTPUTS</span></span>

### <span data-ttu-id="bd0e0-138">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="bd0e0-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="bd0e0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd0e0-139">NOTES</span></span>

## <span data-ttu-id="bd0e0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd0e0-140">RELATED LINKS</span></span>
