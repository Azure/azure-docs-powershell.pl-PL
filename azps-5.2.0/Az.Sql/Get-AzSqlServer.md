---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350134"
---
# <span data-ttu-id="758fe-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="758fe-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="758fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="758fe-102">SYNOPSIS</span></span>
<span data-ttu-id="758fe-103">Zwraca informacje o serwerach baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="758fe-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="758fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="758fe-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="758fe-105">DESCRIPTION</span></span>
<span data-ttu-id="758fe-106">Polecenie cmdlet **Get-AzSqlServer** zwraca informacje dotyczące co najmniej jednego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="758fe-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="758fe-107">Określ nazwę serwera, aby wyświetlić informacje dotyczące tylko tego serwera.</span><span class="sxs-lookup"><span data-stu-id="758fe-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="758fe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="758fe-108">EXAMPLES</span></span>

### <span data-ttu-id="758fe-109">Przykład 1: pobieranie wszystkich wystąpień programu SQL Server przydzielonych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="758fe-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="758fe-110">To polecenie pobiera informacje o wszystkich serwerach bazy danych SQL platformy Azure przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="758fe-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="758fe-111">Przykład 2: uzyskiwanie informacji na temat serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="758fe-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="758fe-112">To polecenie pobiera informacje o serwerze bazy danych SQL Azure o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="758fe-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="758fe-113">Przykład 3: pobieranie wszystkich wystąpień programu SQL Server w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="758fe-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="758fe-114">To polecenie pobiera informacje o wszystkich serwerach bazy danych SQL platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="758fe-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="758fe-115">Przykład 4: pobieranie wszystkich wystąpień programu SQL Server przydzielonych do grupy zasobów przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="758fe-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="758fe-116">To polecenie pobiera informacje o wszystkich serwerach bazy danych SQL platformy Azure przypisanych do grupy zasobów ResourceGroup01, która rozpoczyna się od "serwera".</span><span class="sxs-lookup"><span data-stu-id="758fe-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="758fe-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="758fe-117">PARAMETERS</span></span>

### <span data-ttu-id="758fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758fe-118">-DefaultProfile</span></span>
<span data-ttu-id="758fe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="758fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="758fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="758fe-121">Określa nazwę grupy zasobów, do której mają przydzielone serwery.</span><span class="sxs-lookup"><span data-stu-id="758fe-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758fe-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="758fe-122">-ServerName</span></span>
<span data-ttu-id="758fe-123">Określa nazwę serwera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758fe-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758fe-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="758fe-124">-Confirm</span></span>
<span data-ttu-id="758fe-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758fe-126">-WhatIf</span></span>
<span data-ttu-id="758fe-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758fe-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="758fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758fe-129">CommonParameters</span></span>
<span data-ttu-id="758fe-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758fe-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="758fe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758fe-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="758fe-132">INPUTS</span></span>

### <span data-ttu-id="758fe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="758fe-133">System.String</span></span>

## <span data-ttu-id="758fe-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="758fe-134">OUTPUTS</span></span>

### <span data-ttu-id="758fe-135">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="758fe-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="758fe-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="758fe-136">NOTES</span></span>

## <span data-ttu-id="758fe-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="758fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="758fe-138">Nowe — AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="758fe-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="758fe-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="758fe-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="758fe-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="758fe-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="758fe-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="758fe-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


