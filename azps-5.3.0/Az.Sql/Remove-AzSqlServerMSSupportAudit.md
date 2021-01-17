---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489518"
---
# <span data-ttu-id="9365c-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="9365c-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="9365c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9365c-102">SYNOPSIS</span></span>
<span data-ttu-id="9365c-103">Usuwa ustawienia inspekcji operacji pomocy technicznej firmy Microsoft dotyczące programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9365c-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="9365c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9365c-104">SYNTAX</span></span>

### <span data-ttu-id="9365c-105">ServerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9365c-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9365c-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9365c-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9365c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9365c-107">DESCRIPTION</span></span>
<span data-ttu-id="9365c-108">Polecenie cmdlet **Remove-AzSqlServerMSSupportAudit** usuwa ustawienia inspekcji operacji pomocy technicznej firmy Microsoft dotyczące programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9365c-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="9365c-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="9365c-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="9365c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9365c-110">EXAMPLES</span></span>

### <span data-ttu-id="9365c-111">Przykład 1: usuwanie ustawień inspekcji operacji pomocy technicznej firmy Microsoft w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9365c-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="9365c-112">Przykład 2: usuwanie za pośrednictwem rurociągu ustawień inspekcji pomocy technicznej firmy Microsoft w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9365c-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="9365c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9365c-113">PARAMETERS</span></span>

### <span data-ttu-id="9365c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9365c-114">-AsJob</span></span>
<span data-ttu-id="9365c-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9365c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9365c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9365c-116">-DefaultProfile</span></span>
<span data-ttu-id="9365c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9365c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9365c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9365c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9365c-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9365c-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9365c-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9365c-120">-ServerName</span></span>
<span data-ttu-id="9365c-121">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="9365c-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9365c-122">-Serverobject</span><span class="sxs-lookup"><span data-stu-id="9365c-122">-ServerObject</span></span>
<span data-ttu-id="9365c-123">Obiekt serwera do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="9365c-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9365c-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9365c-124">-Confirm</span></span>
<span data-ttu-id="9365c-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9365c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9365c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9365c-126">-WhatIf</span></span>
<span data-ttu-id="9365c-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9365c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9365c-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9365c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9365c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9365c-129">CommonParameters</span></span>
<span data-ttu-id="9365c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9365c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9365c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9365c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9365c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9365c-132">INPUTS</span></span>

### <span data-ttu-id="9365c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9365c-133">System.String</span></span>

### <span data-ttu-id="9365c-134">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9365c-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9365c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9365c-135">OUTPUTS</span></span>

### <span data-ttu-id="9365c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9365c-136">System.Boolean</span></span>

## <span data-ttu-id="9365c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9365c-137">NOTES</span></span>

## <span data-ttu-id="9365c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9365c-138">RELATED LINKS</span></span>
