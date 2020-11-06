---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542163"
---
# <span data-ttu-id="fdf22-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf22-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="fdf22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdf22-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf22-103">Ustawia maskowanie danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdf22-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf22-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fdf22-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf22-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseDataMaskingPolicy** ustawia zasady maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fdf22-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="fdf22-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fdf22-108">Parametr *DataMaskingState* można ustawić w celu określenia, czy operacje maskowania danych są włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fdf22-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="fdf22-109">Możesz również ustawić parametr *PrivilegedLogins* , aby określić, którzy użytkownicy mogą wyświetlać niezamaskowane dane.</span><span class="sxs-lookup"><span data-stu-id="fdf22-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="fdf22-110">Jeśli polecenie cmdlet jest poprawne i użyto parametru *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady maskowania danych oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="fdf22-111">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="fdf22-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="fdf22-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf22-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fdf22-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdf22-113">EXAMPLES</span></span>

### <span data-ttu-id="fdf22-114">Przykład 1. Ustawianie zasad maskowania danych dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="fdf22-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="fdf22-115">To polecenie ustawia zasady maskowania danych dla bazy danych o nazwie database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="fdf22-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="fdf22-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdf22-116">PARAMETERS</span></span>

### <span data-ttu-id="fdf22-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fdf22-117">-DatabaseName</span></span>
<span data-ttu-id="fdf22-118">Określa nazwę bazy danych, w której ustawiono zasadę.</span><span class="sxs-lookup"><span data-stu-id="fdf22-118">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="fdf22-119">-DataMaskingState</span></span>
<span data-ttu-id="fdf22-120">Określa, czy operacja maskowania danych jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="fdf22-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="fdf22-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fdf22-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdf22-122">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="fdf22-122">Enabled</span></span>
- <span data-ttu-id="fdf22-123">Łącza</span><span class="sxs-lookup"><span data-stu-id="fdf22-123">Disabled</span></span>

<span data-ttu-id="fdf22-124">Wartość domyślna jest włączona.</span><span class="sxs-lookup"><span data-stu-id="fdf22-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf22-125">-DefaultProfile</span></span>
<span data-ttu-id="fdf22-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fdf22-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf22-127">-PassThru</span></span>
<span data-ttu-id="fdf22-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fdf22-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fdf22-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="fdf22-130">-PrivilegedLogins</span></span>
<span data-ttu-id="fdf22-131">Określa, którzy użytkownicy SQL wykluczeni z maskowania.</span><span class="sxs-lookup"><span data-stu-id="fdf22-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="fdf22-132">Ten parametr jest przestarzały i zostanie usunięty z przyszłych wersji.</span><span class="sxs-lookup"><span data-stu-id="fdf22-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="fdf22-133">-PrivilegedUsers</span></span>
<span data-ttu-id="fdf22-134">Określa rozdzielaną średnikami listę identyfikatorów użytkowników uprzywilejowanych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="fdf22-135">Ci użytkownicy mogą wyświetlać dane maskowania.</span><span class="sxs-lookup"><span data-stu-id="fdf22-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf22-136">-ResourceGroupName</span></span>
<span data-ttu-id="fdf22-137">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-137">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fdf22-138">-ServerName</span></span>
<span data-ttu-id="fdf22-139">Określa nazwę serwera obsługującego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-139">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdf22-140">-Confirm</span></span>
<span data-ttu-id="fdf22-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf22-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf22-142">-WhatIf</span></span>
<span data-ttu-id="fdf22-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf22-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdf22-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdf22-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf22-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf22-145">CommonParameters</span></span>
<span data-ttu-id="fdf22-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf22-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf22-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf22-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf22-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdf22-148">INPUTS</span></span>

### <span data-ttu-id="fdf22-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fdf22-149">None</span></span>
<span data-ttu-id="fdf22-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fdf22-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdf22-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdf22-151">OUTPUTS</span></span>

### <span data-ttu-id="fdf22-152">Microsoft. Azure. Commands. SQL. Security. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fdf22-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="fdf22-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdf22-153">NOTES</span></span>

## <span data-ttu-id="fdf22-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdf22-154">RELATED LINKS</span></span>

[<span data-ttu-id="fdf22-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf22-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="fdf22-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fdf22-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fdf22-157">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fdf22-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fdf22-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fdf22-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fdf22-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fdf22-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fdf22-160">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fdf22-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


