---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 3e43a61c95120b0f07f89e3f3fb64aab2dee8dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546404"
---
# <span data-ttu-id="b7b2f-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="b7b2f-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="b7b2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b2f-103">Usuwa inspekcję programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7b2f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b2f-106">Polecenie cmdlet **Remove-AzureRmSqlServerAuditing** umożliwia usunięcie inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="b7b2f-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="b7b2f-108">Po uruchomieniu tego polecenia cmdlet Inspekcja baz danych w usłudze Azure SQL Server nie jest wykonywana.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="b7b2f-109">Jeśli wykonanie polecenia powiedzie się, a następnie określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący bieżące zasady inspekcji i identyfikatory programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="b7b2f-110">Identyfikatory serwera obejmują **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="b7b2f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7b2f-111">EXAMPLES</span></span>

### <span data-ttu-id="b7b2f-112">Przykład 1: usuwanie inspekcji usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b7b2f-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlServerAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="b7b2f-113">To polecenie usuwa inspekcję wszystkich baz danych znajdujących się w Server01 w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="b7b2f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7b2f-114">PARAMETERS</span></span>

### <span data-ttu-id="b7b2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b2f-115">-DefaultProfile</span></span>
<span data-ttu-id="b7b2f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b7b2f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7b2f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7b2f-117">-PassThru</span></span>
<span data-ttu-id="b7b2f-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7b2f-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7b2f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b2f-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7b2f-121">Określa nazwę grupy zasobów, do której jest przypisany Program Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="b7b2f-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b7b2f-122">-ServerName</span></span>
<span data-ttu-id="b7b2f-123">Określa nazwę programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b2f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7b2f-124">-Confirm</span></span>
<span data-ttu-id="b7b2f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b2f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b2f-126">-WhatIf</span></span>
<span data-ttu-id="b7b2f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b2f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b2f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b2f-129">CommonParameters</span></span>
<span data-ttu-id="b7b2f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b2f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b2f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b2f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b2f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7b2f-132">INPUTS</span></span>

### <span data-ttu-id="b7b2f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b2f-133">System.String</span></span>

## <span data-ttu-id="b7b2f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7b2f-134">OUTPUTS</span></span>

### <span data-ttu-id="b7b2f-135">Microsoft. Azure. Commands. SQL. Audit. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7b2f-135">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="b7b2f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7b2f-136">NOTES</span></span>

## <span data-ttu-id="b7b2f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7b2f-137">RELATED LINKS</span></span>

[<span data-ttu-id="b7b2f-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b7b2f-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b7b2f-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b7b2f-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b7b2f-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b7b2f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


