---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: d710137307817223df8cefec6767fecb332bfc3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995156"
---
# <span data-ttu-id="56dc8-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="56dc8-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="56dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="56dc8-103">Usuwa ustawienia inspekcji operacji pomocy technicznej firmy Microsoft serwera Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="56dc8-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="56dc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56dc8-104">SYNTAX</span></span>

### <span data-ttu-id="56dc8-105">ServerParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="56dc8-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56dc8-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56dc8-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56dc8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="56dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="56dc8-108">Polecenie **cmdlet Remove-AzSqlServerMSSupportAudit** usuwa ustawienia inspekcji operacji pomocy technicznej firmy Microsoft serwera Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="56dc8-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="56dc8-109">Aby użyć polecenia cmdlet, określ serwer za pomocą parametrów *ResourceGroupName* i *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="56dc8-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="56dc8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56dc8-110">EXAMPLES</span></span>

### <span data-ttu-id="56dc8-111">Przykład 1. Usunięcie ustawień inspekcji operacji pomocy technicznej firmy Microsoft serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="56dc8-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="56dc8-112">Przykład 2. Usuwanie za pośrednictwem potoku ustawień inspekcji serwera Azure SQL przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="56dc8-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="56dc8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56dc8-113">PARAMETERS</span></span>

### <span data-ttu-id="56dc8-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="56dc8-114">-AsJob</span></span>
<span data-ttu-id="56dc8-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="56dc8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56dc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56dc8-116">-DefaultProfile</span></span>
<span data-ttu-id="56dc8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56dc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56dc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56dc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="56dc8-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56dc8-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="56dc8-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56dc8-120">-ServerName</span></span>
<span data-ttu-id="56dc8-121">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="56dc8-121">SQL server name.</span></span>

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

### <span data-ttu-id="56dc8-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="56dc8-122">-ServerObject</span></span>
<span data-ttu-id="56dc8-123">Obiekt serwera do zarządzania jego zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="56dc8-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="56dc8-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56dc8-124">-Confirm</span></span>
<span data-ttu-id="56dc8-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56dc8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56dc8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56dc8-126">-WhatIf</span></span>
<span data-ttu-id="56dc8-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56dc8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56dc8-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56dc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56dc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56dc8-129">CommonParameters</span></span>
<span data-ttu-id="56dc8-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56dc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56dc8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56dc8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56dc8-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56dc8-132">INPUTS</span></span>

### <span data-ttu-id="56dc8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="56dc8-133">System.String</span></span>

### <span data-ttu-id="56dc8-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="56dc8-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="56dc8-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56dc8-135">OUTPUTS</span></span>

### <span data-ttu-id="56dc8-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56dc8-136">System.Boolean</span></span>

## <span data-ttu-id="56dc8-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56dc8-137">NOTES</span></span>

## <span data-ttu-id="56dc8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56dc8-138">RELATED LINKS</span></span>
