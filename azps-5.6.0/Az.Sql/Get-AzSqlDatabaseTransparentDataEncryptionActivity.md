---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0bdfa7ddf86beef3b9db26ff36a1953a1b574fd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014714"
---
# <span data-ttu-id="8069a-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="8069a-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="8069a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8069a-102">SYNOPSIS</span></span>
<span data-ttu-id="8069a-103">Pobiera postęp skanowania TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8069a-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="8069a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8069a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8069a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8069a-105">DESCRIPTION</span></span>
<span data-ttu-id="8069a-106">Polecenie **cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity** pobiera postęp skanowania przezroczystego szyfrowania danych (TDE, Transparent Data Encryption) bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="8069a-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="8069a-107">Jeśli nie jest uruchomione żadne szyfrowanie, to polecenie cmdlet zwraca pustą listę.</span><span class="sxs-lookup"><span data-stu-id="8069a-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="8069a-108">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych przy użyciu usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (w bibliotece Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="8069a-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="8069a-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8069a-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8069a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8069a-110">EXAMPLES</span></span>

### <span data-ttu-id="8069a-111">Przykład 1. Uzyskiwanie aktywności TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="8069a-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="8069a-112">To polecenie pobiera działanie TDE dla bazy danych o nazwie database01 na serwerze o nazwie serwer01.</span><span class="sxs-lookup"><span data-stu-id="8069a-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="8069a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8069a-113">PARAMETERS</span></span>

### <span data-ttu-id="8069a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8069a-114">-DatabaseName</span></span>
<span data-ttu-id="8069a-115">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera aktywność szyfrowania TDE.</span><span class="sxs-lookup"><span data-stu-id="8069a-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="8069a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8069a-116">-DefaultProfile</span></span>
<span data-ttu-id="8069a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8069a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8069a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8069a-118">-ResourceGroupName</span></span>
<span data-ttu-id="8069a-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="8069a-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8069a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8069a-120">-ServerName</span></span>
<span data-ttu-id="8069a-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="8069a-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8069a-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8069a-122">-Confirm</span></span>
<span data-ttu-id="8069a-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8069a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8069a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8069a-124">-WhatIf</span></span>
<span data-ttu-id="8069a-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8069a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8069a-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8069a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8069a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8069a-127">CommonParameters</span></span>
<span data-ttu-id="8069a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8069a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8069a-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8069a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8069a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8069a-130">INPUTS</span></span>

### <span data-ttu-id="8069a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8069a-131">System.String</span></span>

## <span data-ttu-id="8069a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8069a-132">OUTPUTS</span></span>

### <span data-ttu-id="8069a-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="8069a-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="8069a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8069a-134">NOTES</span></span>

## <span data-ttu-id="8069a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8069a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8069a-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="8069a-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="8069a-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="8069a-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


