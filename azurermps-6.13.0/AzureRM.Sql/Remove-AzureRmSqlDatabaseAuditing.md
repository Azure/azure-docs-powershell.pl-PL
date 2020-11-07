---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a7cf769b1150ef7e209bd02234674bb26927f9a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547324"
---
# <span data-ttu-id="fa50f-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fa50f-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="fa50f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa50f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa50f-103">Usuwa inspekcję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa50f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa50f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa50f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa50f-105">DESCRIPTION</span></span>
<span data-ttu-id="fa50f-106">Polecenie cmdlet **Remove-AzureRmSqlDatabaseAuditing** usuwa inspekcję bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fa50f-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="fa50f-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fa50f-108">Po uruchomieniu tego polecenia cmdlet Inspekcja bazy danych nie jest przeprowadzana.</span><span class="sxs-lookup"><span data-stu-id="fa50f-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="fa50f-109">Jeśli wykonanie polecenia powiedzie się i użyto parametru *PassThru* , polecenie cmdlet zwróci obiekt opisujący bieżące zasady inspekcji oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="fa50f-110">Identyfikatory bazy danych obejmują, ale nie są ograniczone do **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="fa50f-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>
<span data-ttu-id="fa50f-111">W przypadku usunięcia inspekcji bazy danych Azure SQL Database wykrywanie zagrożeń również zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="fa50f-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>
<span data-ttu-id="fa50f-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fa50f-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fa50f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa50f-113">EXAMPLES</span></span>

### <span data-ttu-id="fa50f-114">Przykład 1: usuwanie inspekcji bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fa50f-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fa50f-115">To polecenie usuwa inspekcję bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="fa50f-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="fa50f-116">Baza danych znajduje się w witrynie Server01, która jest przypisana do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fa50f-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fa50f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa50f-117">PARAMETERS</span></span>

### <span data-ttu-id="fa50f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa50f-118">-DatabaseName</span></span>
<span data-ttu-id="fa50f-119">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fa50f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa50f-120">-DefaultProfile</span></span>
<span data-ttu-id="fa50f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fa50f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa50f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa50f-122">-PassThru</span></span>
<span data-ttu-id="fa50f-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fa50f-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fa50f-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa50f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa50f-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa50f-126">Określa nazwę grupy zasobów zawierającej bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="fa50f-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fa50f-127">-ServerName</span></span>
<span data-ttu-id="fa50f-128">Określa nazwę serwera zawierającego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fa50f-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="fa50f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa50f-129">-Confirm</span></span>
<span data-ttu-id="fa50f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa50f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa50f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa50f-131">-WhatIf</span></span>
<span data-ttu-id="fa50f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa50f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa50f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa50f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa50f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa50f-134">CommonParameters</span></span>
<span data-ttu-id="fa50f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa50f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa50f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa50f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa50f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa50f-137">INPUTS</span></span>

### <span data-ttu-id="fa50f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fa50f-138">System.String</span></span>

## <span data-ttu-id="fa50f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa50f-139">OUTPUTS</span></span>

### <span data-ttu-id="fa50f-140">Microsoft. Azure. Commands. SQL. Audit. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fa50f-140">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="fa50f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa50f-141">NOTES</span></span>

## <span data-ttu-id="fa50f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa50f-142">RELATED LINKS</span></span>

[<span data-ttu-id="fa50f-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa50f-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fa50f-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa50f-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fa50f-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fa50f-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

