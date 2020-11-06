---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8b0f66ceb624689ad66a9ab8fa4bbf9d0fcb2391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525994"
---
# <span data-ttu-id="bd31d-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bd31d-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="bd31d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd31d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd31d-103">Umożliwia utworzenie łącza komunikacyjnego dla transakcji Elastic Database między dwoma serwerami baz danych SQL.</span><span class="sxs-lookup"><span data-stu-id="bd31d-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd31d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd31d-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd31d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd31d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd31d-106">Polecenie cmdlet **New-AzureRmSqlServerCommunicationLink** tworzy łącze komunikacyjne dla transakcji Elastic Database między dwoma serwerami logicznymi w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd31d-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="bd31d-107">Transakcje Elastic Database mogą obejmować bazy danych w jednym z sparowanych serwerów.</span><span class="sxs-lookup"><span data-stu-id="bd31d-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="bd31d-108">Na serwerze można utworzyć więcej niż jedno łącze.</span><span class="sxs-lookup"><span data-stu-id="bd31d-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="bd31d-109">W związku z tym transakcje elastycznej bazy danych mogą obejmować większą liczbę serwerów.</span><span class="sxs-lookup"><span data-stu-id="bd31d-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="bd31d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd31d-110">EXAMPLES</span></span>

### <span data-ttu-id="bd31d-111">Przykład 1. Tworzenie łącza komunikacyjnego</span><span class="sxs-lookup"><span data-stu-id="bd31d-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="bd31d-112">To polecenie tworzy link o nazwie Link01 między ContosoServer17 i ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="bd31d-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="bd31d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd31d-113">PARAMETERS</span></span>

### <span data-ttu-id="bd31d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd31d-114">-AsJob</span></span>
<span data-ttu-id="bd31d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bd31d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd31d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd31d-116">-DefaultProfile</span></span>
<span data-ttu-id="bd31d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bd31d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd31d-118">-Linkname</span><span class="sxs-lookup"><span data-stu-id="bd31d-118">-LinkName</span></span>
<span data-ttu-id="bd31d-119">Określa nazwę linku komunikacyjnego serwera tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd31d-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bd31d-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="bd31d-120">-PartnerServer</span></span>
<span data-ttu-id="bd31d-121">Określa nazwę drugiego serwera, który bierze udział w tym łączu komunikacyjnym.</span><span class="sxs-lookup"><span data-stu-id="bd31d-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="bd31d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd31d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd31d-123">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="bd31d-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="bd31d-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="bd31d-124">-ServerName</span></span>
<span data-ttu-id="bd31d-125">Określa nazwę serwera, na którym ten aplet polecenia konfiguruje łącze komunikacyjne.</span><span class="sxs-lookup"><span data-stu-id="bd31d-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="bd31d-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd31d-126">-Confirm</span></span>
<span data-ttu-id="bd31d-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd31d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd31d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd31d-128">-WhatIf</span></span>
<span data-ttu-id="bd31d-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd31d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd31d-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd31d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd31d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd31d-131">CommonParameters</span></span>
<span data-ttu-id="bd31d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd31d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd31d-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd31d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd31d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd31d-134">INPUTS</span></span>

### <span data-ttu-id="bd31d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bd31d-135">System.String</span></span>

## <span data-ttu-id="bd31d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd31d-136">OUTPUTS</span></span>

### <span data-ttu-id="bd31d-137">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="bd31d-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="bd31d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd31d-138">NOTES</span></span>
* <span data-ttu-id="bd31d-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="bd31d-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="bd31d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd31d-140">RELATED LINKS</span></span>

[<span data-ttu-id="bd31d-141">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bd31d-141">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="bd31d-142">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bd31d-142">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="bd31d-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="bd31d-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
