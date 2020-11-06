---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527773"
---
# <span data-ttu-id="b7124-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b7124-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="b7124-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7124-102">SYNOPSIS</span></span>
<span data-ttu-id="b7124-103">Ustawia maskowanie danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7124-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7124-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7124-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7124-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7124-105">DESCRIPTION</span></span>
<span data-ttu-id="b7124-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseDataMaskingPolicy** ustawia zasady maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b7124-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="b7124-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7124-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b7124-108">Parametr *DataMaskingState* można ustawić w celu określenia, czy operacje maskowania danych są włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="b7124-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="b7124-109">Możesz również ustawić parametr *PrivilegedLogins* , aby określić, którzy użytkownicy mogą wyświetlać niezamaskowane dane.</span><span class="sxs-lookup"><span data-stu-id="b7124-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="b7124-110">Jeśli polecenie cmdlet jest poprawne i użyto parametru *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady maskowania danych oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7124-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b7124-111">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="b7124-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="b7124-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b7124-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b7124-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7124-113">EXAMPLES</span></span>

### <span data-ttu-id="b7124-114">Przykład 1. Ustawianie zasad maskowania danych dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="b7124-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="b7124-115">To polecenie ustawia zasady maskowania danych dla bazy danych o nazwie database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="b7124-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="b7124-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7124-116">PARAMETERS</span></span>

### <span data-ttu-id="b7124-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7124-117">-DatabaseName</span></span>
<span data-ttu-id="b7124-118">Określa nazwę bazy danych, w której ustawiono zasadę.</span><span class="sxs-lookup"><span data-stu-id="b7124-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="b7124-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="b7124-119">-DataMaskingState</span></span>
<span data-ttu-id="b7124-120">Określa, czy operacja maskowania danych jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="b7124-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="b7124-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7124-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7124-122">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="b7124-122">Enabled</span></span>
- <span data-ttu-id="b7124-123">Wyłączona wartość domyślna jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b7124-123">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="b7124-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7124-124">-DefaultProfile</span></span>
<span data-ttu-id="b7124-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b7124-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7124-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7124-126">-PassThru</span></span>
<span data-ttu-id="b7124-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b7124-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7124-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b7124-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7124-129">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="b7124-129">-PrivilegedLogins</span></span>
<span data-ttu-id="b7124-130">Określa, którzy użytkownicy SQL wykluczeni z maskowania.</span><span class="sxs-lookup"><span data-stu-id="b7124-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="b7124-131">Ten parametr jest przestarzały i zostanie usunięty z przyszłych wersji.</span><span class="sxs-lookup"><span data-stu-id="b7124-131">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="b7124-132">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="b7124-132">-PrivilegedUsers</span></span>
<span data-ttu-id="b7124-133">Określa rozdzielaną średnikami listę identyfikatorów użytkowników uprzywilejowanych.</span><span class="sxs-lookup"><span data-stu-id="b7124-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="b7124-134">Ci użytkownicy mogą wyświetlać dane maskowania.</span><span class="sxs-lookup"><span data-stu-id="b7124-134">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="b7124-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7124-135">-ResourceGroupName</span></span>
<span data-ttu-id="b7124-136">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b7124-136">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b7124-137">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b7124-137">-ServerName</span></span>
<span data-ttu-id="b7124-138">Określa nazwę serwera obsługującego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b7124-138">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="b7124-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7124-139">-Confirm</span></span>
<span data-ttu-id="b7124-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7124-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7124-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7124-141">-WhatIf</span></span>
<span data-ttu-id="b7124-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7124-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7124-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7124-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7124-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7124-144">CommonParameters</span></span>
<span data-ttu-id="b7124-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7124-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7124-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7124-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7124-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7124-147">INPUTS</span></span>

### <span data-ttu-id="b7124-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b7124-148">System.String</span></span>

## <span data-ttu-id="b7124-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7124-149">OUTPUTS</span></span>

### <span data-ttu-id="b7124-150">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7124-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="b7124-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7124-151">NOTES</span></span>

## <span data-ttu-id="b7124-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7124-152">RELATED LINKS</span></span>

[<span data-ttu-id="b7124-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b7124-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b7124-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b7124-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b7124-155">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b7124-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b7124-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b7124-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b7124-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b7124-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b7124-158">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b7124-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


