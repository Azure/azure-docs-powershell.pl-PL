---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: c9e3f55940f77d4627f4e3e4f7e9a26f47606206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707804"
---
# <span data-ttu-id="7b5f4-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7b5f4-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="7b5f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5f4-103">Umożliwia usunięcie łącza komunikacyjnego dla transakcji Elastic Database między dwoma serwerami.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="7b5f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b5f4-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b5f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5f4-106">Polecenie cmdlet **Remove-AzSqlServerCommunicationLink** usuwa link komunikacji między serwerami dla transakcji Elastic Database w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="7b5f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b5f4-107">EXAMPLES</span></span>

### <span data-ttu-id="7b5f4-108">Przykład 1: Usuwanie łącza komunikacyjnego</span><span class="sxs-lookup"><span data-stu-id="7b5f4-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="7b5f4-109">To polecenie powoduje usunięcie linku komunikacyjnego serwer-do-serwera o nazwie Link01 na ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="7b5f4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b5f4-110">PARAMETERS</span></span>

### <span data-ttu-id="7b5f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5f4-111">-DefaultProfile</span></span>
<span data-ttu-id="7b5f4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7b5f4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b5f4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7b5f4-113">-Force</span></span>
<span data-ttu-id="7b5f4-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b5f4-115">-Linkname</span><span class="sxs-lookup"><span data-stu-id="7b5f4-115">-LinkName</span></span>
<span data-ttu-id="7b5f4-116">Określa nazwę łącza komunikacyjnego serwera, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7b5f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b5f4-118">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="7b5f4-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="7b5f4-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7b5f4-119">-ServerName</span></span>
<span data-ttu-id="7b5f4-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-120">Specifies the name of a server.</span></span>
<span data-ttu-id="7b5f4-121">Ten serwer zawiera łącze komunikacyjne, które zostało usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7b5f4-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b5f4-122">-Confirm</span></span>
<span data-ttu-id="7b5f4-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b5f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5f4-124">-WhatIf</span></span>
<span data-ttu-id="7b5f4-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b5f4-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b5f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5f4-127">CommonParameters</span></span>
<span data-ttu-id="7b5f4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5f4-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b5f4-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5f4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b5f4-130">INPUTS</span></span>

### <span data-ttu-id="7b5f4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7b5f4-131">System.String</span></span>

## <span data-ttu-id="7b5f4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b5f4-132">OUTPUTS</span></span>

### <span data-ttu-id="7b5f4-133">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="7b5f4-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="7b5f4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b5f4-134">NOTES</span></span>
* <span data-ttu-id="7b5f4-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7b5f4-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7b5f4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b5f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="7b5f4-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7b5f4-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="7b5f4-138">Nowe — AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7b5f4-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="7b5f4-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7b5f4-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)