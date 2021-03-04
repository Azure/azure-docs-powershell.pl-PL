---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d84a954fc6ca6531f1f485baf2cd8006c8a509bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952993"
---
# <span data-ttu-id="ddf7e-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ddf7e-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ddf7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf7e-103">Pobiera zasady maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="ddf7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddf7e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddf7e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddf7e-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf7e-106">Polecenie **cmdlet Get-AzSqlDatabaseDataMaskingPolicy** pobiera zasady maskowania danych w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="ddf7e-107">Aby użyć tego polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="ddf7e-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ddf7e-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ddf7e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddf7e-109">EXAMPLES</span></span>

### <span data-ttu-id="ddf7e-110">Przykład 1. Uzyskiwanie zasad maskowania danych dla bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ddf7e-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="ddf7e-111">To polecenie pobiera zasady maskowania danych z bazy danych Database01 w grupie zasobów ResourceGroup01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="ddf7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf7e-112">PARAMETERS</span></span>

### <span data-ttu-id="ddf7e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddf7e-113">-DatabaseName</span></span>
<span data-ttu-id="ddf7e-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-114">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf7e-115">-DefaultProfile</span></span>
<span data-ttu-id="ddf7e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ddf7e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddf7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ddf7e-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf7e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ddf7e-119">-ServerName</span></span>
<span data-ttu-id="ddf7e-120">Określa nazwę serwera, na którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-120">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf7e-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddf7e-121">-Confirm</span></span>
<span data-ttu-id="ddf7e-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf7e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf7e-123">-WhatIf</span></span>
<span data-ttu-id="ddf7e-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf7e-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf7e-126">CommonParameters</span></span>
<span data-ttu-id="ddf7e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf7e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddf7e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf7e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddf7e-129">INPUTS</span></span>

### <span data-ttu-id="ddf7e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf7e-130">System.String</span></span>

## <span data-ttu-id="ddf7e-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddf7e-131">OUTPUTS</span></span>

### <span data-ttu-id="ddf7e-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ddf7e-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ddf7e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddf7e-133">NOTES</span></span>

## <span data-ttu-id="ddf7e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddf7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="ddf7e-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddf7e-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddf7e-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddf7e-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddf7e-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddf7e-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddf7e-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ddf7e-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ddf7e-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddf7e-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


