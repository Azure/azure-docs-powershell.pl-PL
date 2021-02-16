---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176770"
---
# <span data-ttu-id="b9a82-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b9a82-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="b9a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a82-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a82-103">Usuwa link komunikacji dla elastycznych transakcji bazy danych między dwoma serwerami.</span><span class="sxs-lookup"><span data-stu-id="b9a82-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="b9a82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9a82-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9a82-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9a82-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a82-106">Polecenie cmdlet **Remove-AzSqlServerCommunicationLink** usuwa link do komunikacji między serwerami w celu elastycznej transakcji bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b9a82-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="b9a82-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9a82-107">EXAMPLES</span></span>

### <span data-ttu-id="b9a82-108">Przykład 1. Usuwanie linku do komunikacji</span><span class="sxs-lookup"><span data-stu-id="b9a82-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="b9a82-109">To polecenie usuwa link do komunikacji między serwerami o nazwie Link01 w usłudze ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="b9a82-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="b9a82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9a82-110">PARAMETERS</span></span>

### <span data-ttu-id="b9a82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a82-111">-DefaultProfile</span></span>
<span data-ttu-id="b9a82-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b9a82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9a82-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b9a82-113">-Force</span></span>
<span data-ttu-id="b9a82-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b9a82-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9a82-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="b9a82-115">-LinkName</span></span>
<span data-ttu-id="b9a82-116">Określa nazwę łącza do komunikacji serwera, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a82-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b9a82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a82-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9a82-118">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="b9a82-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="b9a82-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9a82-119">-ServerName</span></span>
<span data-ttu-id="b9a82-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="b9a82-120">Specifies the name of a server.</span></span>
<span data-ttu-id="b9a82-121">Ten serwer zawiera link do komunikacji, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a82-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b9a82-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9a82-122">-Confirm</span></span>
<span data-ttu-id="b9a82-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b9a82-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a82-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a82-124">-WhatIf</span></span>
<span data-ttu-id="b9a82-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a82-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a82-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b9a82-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a82-127">CommonParameters</span></span>
<span data-ttu-id="b9a82-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a82-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9a82-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a82-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9a82-130">INPUTS</span></span>

### <span data-ttu-id="b9a82-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9a82-131">System.String</span></span>

## <span data-ttu-id="b9a82-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a82-132">OUTPUTS</span></span>

### <span data-ttu-id="b9a82-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b9a82-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="b9a82-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9a82-134">NOTES</span></span>
* <span data-ttu-id="b9a82-135">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="b9a82-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b9a82-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9a82-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9a82-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b9a82-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b9a82-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b9a82-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b9a82-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b9a82-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
