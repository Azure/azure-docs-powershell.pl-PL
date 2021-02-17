---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176906"
---
# <span data-ttu-id="eefd1-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="eefd1-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="eefd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefd1-102">SYNOPSIS</span></span>
<span data-ttu-id="eefd1-103">Pobiera linki komunikacyjne do elastycznych transakcji bazy danych między serwerami baz danych.</span><span class="sxs-lookup"><span data-stu-id="eefd1-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="eefd1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eefd1-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefd1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eefd1-105">DESCRIPTION</span></span>
<span data-ttu-id="eefd1-106">Polecenie **cmdlet Get-AzSqlServerCommunicationLink** pobiera linki komunikacji między serwerami w celu elastycznej transakcji bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="eefd1-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="eefd1-107">Określ nazwę linku do komunikacji serwera, aby wyświetlić właściwości tego linku.</span><span class="sxs-lookup"><span data-stu-id="eefd1-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="eefd1-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eefd1-108">EXAMPLES</span></span>

### <span data-ttu-id="eefd1-109">Przykład 1. Uzyskiwanie wszystkich łączy komunikacyjnych dla serwera</span><span class="sxs-lookup"><span data-stu-id="eefd1-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="eefd1-110">To polecenie pobiera wszystkie linki komunikacyjne między serwerami dla elastycznych transakcji bazy danych dla serwera o nazwie ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="eefd1-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="eefd1-111">Przykład 2. Uzyskiwanie określonego linku do komunikacji dla serwera</span><span class="sxs-lookup"><span data-stu-id="eefd1-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="eefd1-112">To polecenie pobiera link do komunikacji między serwerami o nazwie Link01.</span><span class="sxs-lookup"><span data-stu-id="eefd1-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="eefd1-113">Przykład 3. Uzyskiwanie wszystkich łączy komunikacyjnych dla serwera przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="eefd1-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="eefd1-114">To polecenie pobiera wszystkie linki komunikacyjne między serwerami dla elastycznych transakcji bazy danych dla serwera o nazwie ContosoServer17, których nazwy zaczynają się od "Link".</span><span class="sxs-lookup"><span data-stu-id="eefd1-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="eefd1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefd1-115">PARAMETERS</span></span>

### <span data-ttu-id="eefd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefd1-116">-DefaultProfile</span></span>
<span data-ttu-id="eefd1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="eefd1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eefd1-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="eefd1-118">-LinkName</span></span>
<span data-ttu-id="eefd1-119">Określa nazwę łącza do komunikacji serwera, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefd1-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefd1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefd1-120">-ResourceGroupName</span></span>
<span data-ttu-id="eefd1-121">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="eefd1-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="eefd1-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eefd1-122">-ServerName</span></span>
<span data-ttu-id="eefd1-123">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="eefd1-123">Specifies the name of a server.</span></span>
<span data-ttu-id="eefd1-124">Ten serwer zawiera link do komunikacji, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefd1-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eefd1-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eefd1-125">-Confirm</span></span>
<span data-ttu-id="eefd1-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eefd1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefd1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefd1-127">-WhatIf</span></span>
<span data-ttu-id="eefd1-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefd1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefd1-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eefd1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefd1-130">CommonParameters</span></span>
<span data-ttu-id="eefd1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefd1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eefd1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefd1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eefd1-133">INPUTS</span></span>

### <span data-ttu-id="eefd1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eefd1-134">System.String</span></span>

## <span data-ttu-id="eefd1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eefd1-135">OUTPUTS</span></span>

### <span data-ttu-id="eefd1-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="eefd1-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="eefd1-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eefd1-137">NOTES</span></span>
* <span data-ttu-id="eefd1-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="eefd1-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="eefd1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eefd1-139">RELATED LINKS</span></span>

[<span data-ttu-id="eefd1-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="eefd1-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="eefd1-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="eefd1-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="eefd1-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="eefd1-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
