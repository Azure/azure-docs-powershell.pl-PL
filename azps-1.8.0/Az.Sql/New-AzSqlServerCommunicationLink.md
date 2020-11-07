---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 8860b4952f11e1d0ad07ca65e6ed77f8fdc2fa5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707852"
---
# <span data-ttu-id="d166c-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d166c-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d166c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d166c-102">SYNOPSIS</span></span>
<span data-ttu-id="d166c-103">Umożliwia utworzenie łącza komunikacyjnego dla transakcji Elastic Database między dwoma serwerami baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d166c-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="d166c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d166c-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d166c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d166c-105">DESCRIPTION</span></span>
<span data-ttu-id="d166c-106">Polecenie cmdlet **New-AzSqlServerCommunicationLink** tworzy łącze komunikacyjne dla transakcji Elastic Database między dwoma serwerami logicznymi w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d166c-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="d166c-107">Transakcje Elastic Database mogą obejmować bazy danych w jednym z sparowanych serwerów.</span><span class="sxs-lookup"><span data-stu-id="d166c-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="d166c-108">Na serwerze można utworzyć więcej niż jedno łącze.</span><span class="sxs-lookup"><span data-stu-id="d166c-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="d166c-109">W związku z tym transakcje elastycznej bazy danych mogą obejmować większą liczbę serwerów.</span><span class="sxs-lookup"><span data-stu-id="d166c-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="d166c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d166c-110">EXAMPLES</span></span>

### <span data-ttu-id="d166c-111">Przykład 1. Tworzenie łącza komunikacyjnego</span><span class="sxs-lookup"><span data-stu-id="d166c-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="d166c-112">To polecenie tworzy link o nazwie Link01 między ContosoServer17 i ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="d166c-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="d166c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d166c-113">PARAMETERS</span></span>

### <span data-ttu-id="d166c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d166c-114">-AsJob</span></span>
<span data-ttu-id="d166c-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d166c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d166c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d166c-116">-DefaultProfile</span></span>
<span data-ttu-id="d166c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d166c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d166c-118">-Linkname</span><span class="sxs-lookup"><span data-stu-id="d166c-118">-LinkName</span></span>
<span data-ttu-id="d166c-119">Określa nazwę linku komunikacyjnego serwera tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d166c-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d166c-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="d166c-120">-PartnerServer</span></span>
<span data-ttu-id="d166c-121">Określa nazwę drugiego serwera, który bierze udział w tym łączu komunikacyjnym.</span><span class="sxs-lookup"><span data-stu-id="d166c-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="d166c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d166c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d166c-123">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="d166c-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d166c-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d166c-124">-ServerName</span></span>
<span data-ttu-id="d166c-125">Określa nazwę serwera, na którym ten aplet polecenia konfiguruje łącze komunikacyjne.</span><span class="sxs-lookup"><span data-stu-id="d166c-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="d166c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d166c-126">-Confirm</span></span>
<span data-ttu-id="d166c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d166c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d166c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d166c-128">-WhatIf</span></span>
<span data-ttu-id="d166c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d166c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d166c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d166c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d166c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d166c-131">CommonParameters</span></span>
<span data-ttu-id="d166c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d166c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d166c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d166c-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d166c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d166c-134">INPUTS</span></span>

### <span data-ttu-id="d166c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d166c-135">System.String</span></span>

## <span data-ttu-id="d166c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d166c-136">OUTPUTS</span></span>

### <span data-ttu-id="d166c-137">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d166c-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d166c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d166c-138">NOTES</span></span>
* <span data-ttu-id="d166c-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d166c-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d166c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d166c-140">RELATED LINKS</span></span>

[<span data-ttu-id="d166c-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d166c-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d166c-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d166c-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d166c-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d166c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
