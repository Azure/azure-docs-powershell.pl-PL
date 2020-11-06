---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ed968db32505bcb3c581775d05235cc4c718dd67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549091"
---
# <span data-ttu-id="ba5b3-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="ba5b3-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="ba5b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5b3-103">Pobiera linki komunikacyjne dotyczące transakcji Elastic Database między serwerami baz danych.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba5b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba5b3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba5b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba5b3-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5b3-106">Polecenie cmdlet **Get-AzureRmSqlServerCommunicationLink** pobiera linki komunikacyjne między serwerami dla transakcji Elastic Database w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="ba5b3-107">Określ nazwę linku komunikacyjnego serwera, aby wyświetlić właściwości tego linku.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="ba5b3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba5b3-108">EXAMPLES</span></span>

### <span data-ttu-id="ba5b3-109">Przykład 1. Uzyskaj wszystkie linki komunikacyjne dla serwera</span><span class="sxs-lookup"><span data-stu-id="ba5b3-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="ba5b3-110">To polecenie uzyskuje wszystkie linki komunikacyjne między serwerami dla transakcji Elastic Database dla serwera o nazwie ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="ba5b3-111">Przykład 2: uzyskiwanie określonego łącza komunikacyjnego dla serwera</span><span class="sxs-lookup"><span data-stu-id="ba5b3-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="ba5b3-112">To polecenie uzyskuje łącze komunikacyjne między serwerami o nazwie Link01.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="ba5b3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba5b3-113">PARAMETERS</span></span>

### <span data-ttu-id="ba5b3-114">-Linkname</span><span class="sxs-lookup"><span data-stu-id="ba5b3-114">-LinkName</span></span>
<span data-ttu-id="ba5b3-115">Określa nazwę linku komunikacyjnego serwera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-115">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba5b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba5b3-117">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="ba5b3-117">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="ba5b3-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba5b3-118">-ServerName</span></span>
<span data-ttu-id="ba5b3-119">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-119">Specifies the name of a server.</span></span>
<span data-ttu-id="ba5b3-120">Ten serwer zawiera link komunikacyjny, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-120">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba5b3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba5b3-121">-Confirm</span></span>
<span data-ttu-id="ba5b3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5b3-123">-WhatIf</span></span>
<span data-ttu-id="ba5b3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5b3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5b3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5b3-126">-DefaultProfile</span></span>
<span data-ttu-id="ba5b3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba5b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5b3-128">CommonParameters</span></span>
<span data-ttu-id="ba5b3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5b3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5b3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba5b3-131">INPUTS</span></span>

## <span data-ttu-id="ba5b3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba5b3-132">OUTPUTS</span></span>

### <span data-ttu-id="ba5b3-133">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ba5b3-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="ba5b3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba5b3-134">NOTES</span></span>
* <span data-ttu-id="ba5b3-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="ba5b3-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="ba5b3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba5b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba5b3-137">Nowe — AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="ba5b3-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="ba5b3-138">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="ba5b3-138">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="ba5b3-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ba5b3-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
