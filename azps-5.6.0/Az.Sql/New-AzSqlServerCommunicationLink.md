---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 79d920f866991cae15e2da08d03e2eecd4d2e91e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969770"
---
# <span data-ttu-id="092f7-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="092f7-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="092f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="092f7-102">SYNOPSIS</span></span>
<span data-ttu-id="092f7-103">Tworzy link komunikacji dla elastycznych transakcji bazy danych między dwoma serwerami usługi SQL Database.</span><span class="sxs-lookup"><span data-stu-id="092f7-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="092f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="092f7-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="092f7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="092f7-105">DESCRIPTION</span></span>
<span data-ttu-id="092f7-106">Polecenie cmdlet **New-AzSqlServerCommunicationLink** tworzy link komunikacji dla elastycznych transakcji bazy danych między dwoma serwerami logicznymi w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="092f7-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="092f7-107">Elastyczne transakcje baz danych mogą obejmować bazy danych na jednym ze sparowanych serwerów.</span><span class="sxs-lookup"><span data-stu-id="092f7-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="092f7-108">Na serwerze można utworzyć więcej niż jedno łącze.</span><span class="sxs-lookup"><span data-stu-id="092f7-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="092f7-109">Dlatego elastyczne transakcje bazy danych mogą obejmować większą liczbę serwerów.</span><span class="sxs-lookup"><span data-stu-id="092f7-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="092f7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="092f7-110">EXAMPLES</span></span>

### <span data-ttu-id="092f7-111">Przykład 1. Tworzenie linku do komunikacji</span><span class="sxs-lookup"><span data-stu-id="092f7-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="092f7-112">To polecenie tworzy link o nazwie Link01 między serwerami ContosoServer17 i ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="092f7-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="092f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="092f7-113">PARAMETERS</span></span>

### <span data-ttu-id="092f7-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="092f7-114">-AsJob</span></span>
<span data-ttu-id="092f7-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="092f7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="092f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092f7-116">-DefaultProfile</span></span>
<span data-ttu-id="092f7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="092f7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="092f7-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="092f7-118">-LinkName</span></span>
<span data-ttu-id="092f7-119">Określa nazwę łącza do komunikacji serwera, które tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="092f7-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092f7-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="092f7-120">-PartnerServer</span></span>
<span data-ttu-id="092f7-121">Określa nazwę innego serwera, który bierze udział w tym linku do komunikacji.</span><span class="sxs-lookup"><span data-stu-id="092f7-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="092f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="092f7-123">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="092f7-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="092f7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="092f7-124">-ServerName</span></span>
<span data-ttu-id="092f7-125">Określa nazwę serwera, na którym to polecenie cmdlet konfiguruje link do komunikacji.</span><span class="sxs-lookup"><span data-stu-id="092f7-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="092f7-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="092f7-126">-Confirm</span></span>
<span data-ttu-id="092f7-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="092f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="092f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="092f7-128">-WhatIf</span></span>
<span data-ttu-id="092f7-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="092f7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="092f7-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="092f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="092f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092f7-131">CommonParameters</span></span>
<span data-ttu-id="092f7-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="092f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092f7-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="092f7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092f7-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="092f7-134">INPUTS</span></span>

### <span data-ttu-id="092f7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="092f7-135">System.String</span></span>

## <span data-ttu-id="092f7-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="092f7-136">OUTPUTS</span></span>

### <span data-ttu-id="092f7-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="092f7-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="092f7-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="092f7-138">NOTES</span></span>
* <span data-ttu-id="092f7-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="092f7-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="092f7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="092f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="092f7-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="092f7-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="092f7-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="092f7-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="092f7-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="092f7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
