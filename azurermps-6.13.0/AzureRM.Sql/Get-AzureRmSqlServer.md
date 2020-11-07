---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a125e3e4580567c403d9541429929f4ba1e638da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544771"
---
# <span data-ttu-id="2a987-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a987-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="2a987-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a987-102">SYNOPSIS</span></span>
<span data-ttu-id="2a987-103">Zwraca informacje o serwerach baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2a987-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a987-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a987-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a987-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a987-105">DESCRIPTION</span></span>
<span data-ttu-id="2a987-106">Polecenie cmdlet **Get-AzureRmSqlServer** zwraca informacje dotyczące co najmniej jednego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2a987-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="2a987-107">Określ nazwę serwera, aby wyświetlić informacje dotyczące tylko tego serwera.</span><span class="sxs-lookup"><span data-stu-id="2a987-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="2a987-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a987-108">EXAMPLES</span></span>

### <span data-ttu-id="2a987-109">Przykład 1: pobieranie wszystkich wystąpień programu SQL Server przydzielonych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2a987-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="2a987-110">To polecenie pobiera informacje o wszystkich serwerach bazy danych SQL platformy Azure przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2a987-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2a987-111">Przykład 2: uzyskiwanie informacji na temat serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="2a987-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="2a987-112">To polecenie pobiera informacje o serwerze bazy danych SQL Azure o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="2a987-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="2a987-113">Przykład 3: pobieranie wszystkich wystąpień programu SQL Server w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a987-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
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

<span data-ttu-id="2a987-114">To polecenie pobiera informacje o wszystkich serwerach bazy danych SQL platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2a987-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="2a987-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a987-115">PARAMETERS</span></span>

### <span data-ttu-id="2a987-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a987-116">-DefaultProfile</span></span>
<span data-ttu-id="2a987-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a987-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a987-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a987-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a987-119">Określa nazwę grupy zasobów, do której mają przydzielone serwery.</span><span class="sxs-lookup"><span data-stu-id="2a987-119">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="2a987-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2a987-120">-ServerName</span></span>
<span data-ttu-id="2a987-121">Określa nazwę serwera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a987-121">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2a987-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a987-122">-Confirm</span></span>
<span data-ttu-id="2a987-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a987-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a987-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a987-124">-WhatIf</span></span>
<span data-ttu-id="2a987-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a987-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a987-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a987-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a987-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a987-127">CommonParameters</span></span>
<span data-ttu-id="2a987-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a987-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a987-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a987-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a987-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a987-130">INPUTS</span></span>

### <span data-ttu-id="2a987-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2a987-131">System.String</span></span>

## <span data-ttu-id="2a987-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a987-132">OUTPUTS</span></span>

### <span data-ttu-id="2a987-133">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="2a987-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2a987-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a987-134">NOTES</span></span>

## <span data-ttu-id="2a987-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a987-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a987-136">Nowe — AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a987-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="2a987-137">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a987-137">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="2a987-138">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2a987-138">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="2a987-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2a987-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

