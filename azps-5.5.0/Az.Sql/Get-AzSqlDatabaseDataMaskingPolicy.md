---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176987"
---
# <span data-ttu-id="ade9c-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ade9c-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ade9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade9c-102">SYNOPSIS</span></span>
<span data-ttu-id="ade9c-103">Pobiera zasady maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ade9c-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="ade9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ade9c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ade9c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ade9c-105">DESCRIPTION</span></span>
<span data-ttu-id="ade9c-106">Polecenie **cmdlet Get-AzSqlDatabaseDataMaskingPolicy** pobiera zasady maskowania danych w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ade9c-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="ade9c-107">Aby użyć tego polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="ade9c-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ade9c-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ade9c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ade9c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ade9c-109">EXAMPLES</span></span>

### <span data-ttu-id="ade9c-110">Przykład 1. Uzyskiwanie zasad maskowania danych dla bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ade9c-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="ade9c-111">To polecenie pobiera zasady maskowania danych z bazy danych Database01 w grupie zasobów ResourceGroup01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="ade9c-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="ade9c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade9c-112">PARAMETERS</span></span>

### <span data-ttu-id="ade9c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ade9c-113">-DatabaseName</span></span>
<span data-ttu-id="ade9c-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ade9c-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ade9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade9c-115">-DefaultProfile</span></span>
<span data-ttu-id="ade9c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ade9c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ade9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ade9c-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="ade9c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ade9c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ade9c-119">-ServerName</span></span>
<span data-ttu-id="ade9c-120">Określa nazwę serwera, na którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="ade9c-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="ade9c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ade9c-121">-Confirm</span></span>
<span data-ttu-id="ade9c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ade9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade9c-123">-WhatIf</span></span>
<span data-ttu-id="ade9c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade9c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ade9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade9c-126">CommonParameters</span></span>
<span data-ttu-id="ade9c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade9c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade9c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade9c-129">INPUTS</span></span>

### <span data-ttu-id="ade9c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ade9c-130">System.String</span></span>

## <span data-ttu-id="ade9c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade9c-131">OUTPUTS</span></span>

### <span data-ttu-id="ade9c-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ade9c-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ade9c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ade9c-133">NOTES</span></span>

## <span data-ttu-id="ade9c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ade9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="ade9c-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ade9c-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ade9c-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ade9c-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ade9c-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ade9c-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ade9c-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ade9c-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ade9c-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ade9c-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


