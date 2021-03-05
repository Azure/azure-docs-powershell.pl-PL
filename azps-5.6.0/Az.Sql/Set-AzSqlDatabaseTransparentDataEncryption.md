---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8e511fa2e83866ac1a0119c410369f7f13705f14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002986"
---
# <span data-ttu-id="a0f97-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a0f97-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="a0f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f97-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f97-103">Modyfikuje właściwość TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a0f97-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="a0f97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0f97-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f97-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0f97-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f97-106">Polecenie **cmdlet Set-AzSqlDatabaseTransparentDataEncryption** modyfikuje właściwość Transparent Data Encryption (TDE) bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a0f97-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="a0f97-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych przy użyciu usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (w bibliotece Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="a0f97-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="a0f97-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f97-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0f97-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0f97-109">EXAMPLES</span></span>

### <span data-ttu-id="a0f97-110">Przykład 1. Włączanie funkcji TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="a0f97-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="a0f97-111">To polecenie włącza TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="a0f97-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="a0f97-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0f97-112">PARAMETERS</span></span>

### <span data-ttu-id="a0f97-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0f97-113">-DatabaseName</span></span>
<span data-ttu-id="a0f97-114">Określa nazwę bazy danych, która zostanie zmodyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f97-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a0f97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f97-115">-DefaultProfile</span></span>
<span data-ttu-id="a0f97-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a0f97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0f97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f97-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0f97-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="a0f97-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a0f97-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0f97-119">-ServerName</span></span>
<span data-ttu-id="a0f97-120">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a0f97-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a0f97-121">— województwo</span><span class="sxs-lookup"><span data-stu-id="a0f97-121">-State</span></span>
<span data-ttu-id="a0f97-122">Określa wartość właściwości TDE.</span><span class="sxs-lookup"><span data-stu-id="a0f97-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="a0f97-123">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a0f97-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0f97-124">Włączone</span><span class="sxs-lookup"><span data-stu-id="a0f97-124">Enabled</span></span> 
- <span data-ttu-id="a0f97-125">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="a0f97-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f97-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0f97-126">-Confirm</span></span>
<span data-ttu-id="a0f97-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a0f97-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f97-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f97-128">-WhatIf</span></span>
<span data-ttu-id="a0f97-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f97-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f97-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a0f97-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f97-131">CommonParameters</span></span>
<span data-ttu-id="a0f97-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f97-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0f97-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f97-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0f97-134">INPUTS</span></span>

### <span data-ttu-id="a0f97-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="a0f97-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="a0f97-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a0f97-136">System.String</span></span>

## <span data-ttu-id="a0f97-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0f97-137">OUTPUTS</span></span>

### <span data-ttu-id="a0f97-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="a0f97-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="a0f97-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0f97-139">NOTES</span></span>

## <span data-ttu-id="a0f97-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0f97-140">RELATED LINKS</span></span>

[<span data-ttu-id="a0f97-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a0f97-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="a0f97-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="a0f97-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="a0f97-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a0f97-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


