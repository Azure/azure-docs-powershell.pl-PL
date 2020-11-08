---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052126"
---
# <span data-ttu-id="4c40d-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="4c40d-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="4c40d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c40d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c40d-103">Usuwa klaster wirtualny usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c40d-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="4c40d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c40d-104">SYNTAX</span></span>

### <span data-ttu-id="4c40d-105">RemoveVirtualClusterFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4c40d-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c40d-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="4c40d-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c40d-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4c40d-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c40d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4c40d-108">DESCRIPTION</span></span>
<span data-ttu-id="4c40d-109">Polecenie cmdlet **Remove-AzSqlVirtualCluster** usuwa klaster wirtualny Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c40d-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="4c40d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c40d-110">EXAMPLES</span></span>

### <span data-ttu-id="4c40d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c40d-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="4c40d-112">To polecenie usuwa klaster wirtualny o nazwie VirtualCluster1 przypisany do ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c40d-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="4c40d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c40d-113">PARAMETERS</span></span>

### <span data-ttu-id="4c40d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c40d-114">-AsJob</span></span>
<span data-ttu-id="4c40d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4c40d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c40d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c40d-116">-DefaultProfile</span></span>
<span data-ttu-id="4c40d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c40d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c40d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c40d-118">-InputObject</span></span>
<span data-ttu-id="4c40d-119">Obiekt wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="4c40d-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c40d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c40d-120">-Name</span></span>
<span data-ttu-id="4c40d-121">Nazwa klastra wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="4c40d-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c40d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c40d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c40d-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c40d-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c40d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c40d-124">-ResourceId</span></span>
<span data-ttu-id="4c40d-125">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="4c40d-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c40d-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c40d-126">-Confirm</span></span>
<span data-ttu-id="4c40d-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c40d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c40d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c40d-128">-WhatIf</span></span>
<span data-ttu-id="4c40d-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c40d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c40d-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c40d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c40d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c40d-131">CommonParameters</span></span>
<span data-ttu-id="4c40d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c40d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c40d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c40d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c40d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c40d-134">INPUTS</span></span>

### <span data-ttu-id="4c40d-135">Microsoft. Azure. Commands. SQL. VirtualCluster. model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="4c40d-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="4c40d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4c40d-136">System.String</span></span>

## <span data-ttu-id="4c40d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c40d-137">OUTPUTS</span></span>

### <span data-ttu-id="4c40d-138">Microsoft. Azure. Commands. SQL. VirtualCluster. model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="4c40d-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="4c40d-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c40d-139">NOTES</span></span>

## <span data-ttu-id="4c40d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c40d-140">RELATED LINKS</span></span>
