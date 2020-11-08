---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225952"
---
# <span data-ttu-id="e91ff-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e91ff-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e91ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e91ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e91ff-103">Pobiera linki komunikacyjne dotyczące transakcji Elastic Database między serwerami baz danych.</span><span class="sxs-lookup"><span data-stu-id="e91ff-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="e91ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e91ff-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e91ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e91ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e91ff-106">Polecenie cmdlet **Get-AzSqlServerCommunicationLink** pobiera linki komunikacyjne między serwerami dla transakcji Elastic Database w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="e91ff-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="e91ff-107">Określ nazwę linku komunikacyjnego serwera, aby wyświetlić właściwości tego linku.</span><span class="sxs-lookup"><span data-stu-id="e91ff-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="e91ff-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e91ff-108">EXAMPLES</span></span>

### <span data-ttu-id="e91ff-109">Przykład 1. Uzyskaj wszystkie linki komunikacyjne dla serwera</span><span class="sxs-lookup"><span data-stu-id="e91ff-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="e91ff-110">To polecenie uzyskuje wszystkie linki komunikacyjne między serwerami dla transakcji Elastic Database dla serwera o nazwie ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="e91ff-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="e91ff-111">Przykład 2: uzyskiwanie określonego łącza komunikacyjnego dla serwera</span><span class="sxs-lookup"><span data-stu-id="e91ff-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="e91ff-112">To polecenie uzyskuje łącze komunikacyjne między serwerami o nazwie Link01.</span><span class="sxs-lookup"><span data-stu-id="e91ff-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="e91ff-113">Przykład 3: uzyskiwanie wszystkich linków komunikacyjnych dla serwera przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="e91ff-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="e91ff-114">To polecenie uzyskuje wszystkie linki komunikacyjne między serwerami dla transakcji Elastic Database dla serwera o nazwie ContosoServer17, które zaczynają się od "link".</span><span class="sxs-lookup"><span data-stu-id="e91ff-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="e91ff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e91ff-115">PARAMETERS</span></span>

### <span data-ttu-id="e91ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91ff-116">-DefaultProfile</span></span>
<span data-ttu-id="e91ff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e91ff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e91ff-118">-Linkname</span><span class="sxs-lookup"><span data-stu-id="e91ff-118">-LinkName</span></span>
<span data-ttu-id="e91ff-119">Określa nazwę linku komunikacyjnego serwera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91ff-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e91ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e91ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="e91ff-121">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="e91ff-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e91ff-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e91ff-122">-ServerName</span></span>
<span data-ttu-id="e91ff-123">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="e91ff-123">Specifies the name of a server.</span></span>
<span data-ttu-id="e91ff-124">Ten serwer zawiera link komunikacyjny, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91ff-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e91ff-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e91ff-125">-Confirm</span></span>
<span data-ttu-id="e91ff-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91ff-127">-WhatIf</span></span>
<span data-ttu-id="e91ff-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e91ff-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e91ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e91ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91ff-130">CommonParameters</span></span>
<span data-ttu-id="e91ff-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91ff-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e91ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91ff-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e91ff-133">INPUTS</span></span>

### <span data-ttu-id="e91ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e91ff-134">System.String</span></span>

## <span data-ttu-id="e91ff-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e91ff-135">OUTPUTS</span></span>

### <span data-ttu-id="e91ff-136">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e91ff-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e91ff-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e91ff-137">NOTES</span></span>
* <span data-ttu-id="e91ff-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="e91ff-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e91ff-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e91ff-139">RELATED LINKS</span></span>

[<span data-ttu-id="e91ff-140">Nowe — AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e91ff-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e91ff-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e91ff-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e91ff-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e91ff-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
