---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222861"
---
# <span data-ttu-id="c8a53-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c8a53-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="c8a53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8a53-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a53-103">Ustawia maskowanie danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="c8a53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8a53-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8a53-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a53-106">Polecenie cmdlet **Set-AzSqlDatabaseDataMaskingPolicy** ustawia zasady maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c8a53-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="c8a53-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c8a53-108">Parametr *DataMaskingState* można ustawić w celu określenia, czy operacje maskowania danych są włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="c8a53-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="c8a53-109">Jeśli polecenie cmdlet jest poprawne i użyto parametru *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady maskowania danych oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="c8a53-110">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="c8a53-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="c8a53-111">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a53-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c8a53-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8a53-112">EXAMPLES</span></span>

### <span data-ttu-id="c8a53-113">Przykład 1. Ustawianie zasad maskowania danych dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="c8a53-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="c8a53-114">To polecenie ustawia zasady maskowania danych dla bazy danych o nazwie database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="c8a53-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="c8a53-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8a53-115">PARAMETERS</span></span>

### <span data-ttu-id="c8a53-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8a53-116">-DatabaseName</span></span>
<span data-ttu-id="c8a53-117">Określa nazwę bazy danych, w której ustawiono zasadę.</span><span class="sxs-lookup"><span data-stu-id="c8a53-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="c8a53-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="c8a53-118">-DataMaskingState</span></span>
<span data-ttu-id="c8a53-119">Określa, czy operacja maskowania danych jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="c8a53-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="c8a53-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c8a53-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8a53-121">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="c8a53-121">Enabled</span></span>
- <span data-ttu-id="c8a53-122">Wyłączona wartość domyślna jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c8a53-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a53-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a53-123">-DefaultProfile</span></span>
<span data-ttu-id="c8a53-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c8a53-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a53-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8a53-125">-PassThru</span></span>
<span data-ttu-id="c8a53-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c8a53-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8a53-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8a53-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="c8a53-128">-PrivilegedUsers</span></span>
<span data-ttu-id="c8a53-129">Określa rozdzielaną średnikami listę identyfikatorów użytkowników uprzywilejowanych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="c8a53-130">Ci użytkownicy mogą wyświetlać dane maskowania.</span><span class="sxs-lookup"><span data-stu-id="c8a53-130">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a53-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a53-131">-ResourceGroupName</span></span>
<span data-ttu-id="c8a53-132">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c8a53-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c8a53-133">-ServerName</span></span>
<span data-ttu-id="c8a53-134">Określa nazwę serwera obsługującego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="c8a53-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="c8a53-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8a53-135">-Confirm</span></span>
<span data-ttu-id="c8a53-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a53-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a53-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a53-137">-WhatIf</span></span>
<span data-ttu-id="c8a53-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a53-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a53-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8a53-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a53-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a53-140">CommonParameters</span></span>
<span data-ttu-id="c8a53-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a53-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a53-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a53-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a53-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8a53-143">INPUTS</span></span>

### <span data-ttu-id="c8a53-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a53-144">System.String</span></span>

## <span data-ttu-id="c8a53-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8a53-145">OUTPUTS</span></span>

### <span data-ttu-id="c8a53-146">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c8a53-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="c8a53-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8a53-147">NOTES</span></span>

## <span data-ttu-id="c8a53-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8a53-148">RELATED LINKS</span></span>

[<span data-ttu-id="c8a53-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c8a53-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="c8a53-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c8a53-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c8a53-151">Nowe — AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c8a53-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c8a53-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c8a53-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c8a53-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c8a53-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c8a53-154">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c8a53-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


