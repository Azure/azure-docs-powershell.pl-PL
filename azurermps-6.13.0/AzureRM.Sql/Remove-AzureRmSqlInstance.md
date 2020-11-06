---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551115"
---
# <span data-ttu-id="26e84-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="26e84-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="26e84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26e84-102">SYNOPSIS</span></span>
<span data-ttu-id="26e84-103">Usuwa wystąpienie bazy danych zarządzanej przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="26e84-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26e84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26e84-104">SYNTAX</span></span>

### <span data-ttu-id="26e84-105">RemoveInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26e84-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e84-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="26e84-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e84-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="26e84-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e84-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26e84-108">DESCRIPTION</span></span>
<span data-ttu-id="26e84-109">Polecenie cmdlet **Remove-AzureRmSqlInstance** umożliwia usunięcie wystąpienia zarządzanego bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26e84-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="26e84-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26e84-110">EXAMPLES</span></span>

### <span data-ttu-id="26e84-111">Przykład 1: usuwanie wystąpienia</span><span class="sxs-lookup"><span data-stu-id="26e84-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="26e84-112">To polecenie powoduje usunięcie wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="26e84-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="26e84-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26e84-113">PARAMETERS</span></span>

### <span data-ttu-id="26e84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e84-114">-DefaultProfile</span></span>
<span data-ttu-id="26e84-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26e84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e84-116">-Force</span><span class="sxs-lookup"><span data-stu-id="26e84-116">-Force</span></span>
<span data-ttu-id="26e84-117">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="26e84-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="26e84-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26e84-118">-InputObject</span></span>
<span data-ttu-id="26e84-119">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="26e84-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26e84-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26e84-120">-Name</span></span>
<span data-ttu-id="26e84-121">Nazwa wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="26e84-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e84-122">-ResourceGroupName</span></span>
<span data-ttu-id="26e84-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26e84-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e84-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e84-124">-ResourceId</span></span>
<span data-ttu-id="26e84-125">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="26e84-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e84-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26e84-126">-Confirm</span></span>
<span data-ttu-id="26e84-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e84-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e84-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e84-128">-WhatIf</span></span>
<span data-ttu-id="26e84-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e84-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e84-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26e84-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e84-131">CommonParameters</span></span>
<span data-ttu-id="26e84-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e84-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e84-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e84-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26e84-134">INPUTS</span></span>

### <span data-ttu-id="26e84-135">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="26e84-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="26e84-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26e84-136">System.String</span></span>

## <span data-ttu-id="26e84-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26e84-137">OUTPUTS</span></span>

### <span data-ttu-id="26e84-138">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="26e84-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="26e84-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26e84-139">NOTES</span></span>

## <span data-ttu-id="26e84-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26e84-140">RELATED LINKS</span></span>
