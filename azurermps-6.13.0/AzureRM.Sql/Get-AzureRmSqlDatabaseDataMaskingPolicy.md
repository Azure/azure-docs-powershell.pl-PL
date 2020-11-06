---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 6b787e3347c20e011193d0b3968e036d53f62226
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548523"
---
# <span data-ttu-id="eaa78-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="eaa78-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="eaa78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaa78-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa78-103">Pobiera zasady maskowania danych dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eaa78-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaa78-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaa78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaa78-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa78-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseDataMaskingPolicy** pobiera zasady maskowania danych bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eaa78-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="eaa78-107">Aby użyć tego polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eaa78-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="eaa78-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa78-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eaa78-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaa78-109">EXAMPLES</span></span>

### <span data-ttu-id="eaa78-110">Przykład 1: pobieranie zasad maskowania danych dla bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="eaa78-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="eaa78-111">To polecenie uzyskuje zasady maskowania danych z bazy danych Database01 w grupie zasób ResourceGroup01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="eaa78-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="eaa78-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaa78-112">PARAMETERS</span></span>

### <span data-ttu-id="eaa78-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eaa78-113">-DatabaseName</span></span>
<span data-ttu-id="eaa78-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eaa78-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="eaa78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa78-115">-DefaultProfile</span></span>
<span data-ttu-id="eaa78-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eaa78-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaa78-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa78-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaa78-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="eaa78-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="eaa78-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="eaa78-119">-ServerName</span></span>
<span data-ttu-id="eaa78-120">Określa nazwę serwera, na którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="eaa78-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="eaa78-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eaa78-121">-Confirm</span></span>
<span data-ttu-id="eaa78-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaa78-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa78-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa78-123">-WhatIf</span></span>
<span data-ttu-id="eaa78-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaa78-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaa78-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eaa78-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa78-126">CommonParameters</span></span>
<span data-ttu-id="eaa78-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa78-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa78-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa78-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaa78-129">INPUTS</span></span>

### <span data-ttu-id="eaa78-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eaa78-130">System.String</span></span>

## <span data-ttu-id="eaa78-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaa78-131">OUTPUTS</span></span>

### <span data-ttu-id="eaa78-132">Microsoft. Azure. Commands. SQL. datamaskowania. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="eaa78-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="eaa78-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaa78-133">NOTES</span></span>

## <span data-ttu-id="eaa78-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaa78-134">RELATED LINKS</span></span>

[<span data-ttu-id="eaa78-135">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eaa78-135">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eaa78-136">Nowe — AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eaa78-136">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eaa78-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eaa78-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="eaa78-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="eaa78-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="eaa78-139">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="eaa78-139">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


