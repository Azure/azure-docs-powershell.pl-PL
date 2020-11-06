---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550499"
---
# <span data-ttu-id="ba6a4-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ba6a4-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="ba6a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6a4-103">Usuwa dany punkt przywracania z bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba6a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba6a4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba6a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6a4-106">Polecenie cmdlet **Remove-AzureRmSqlDatabaseRestorePoint** usuwa dany punkt przywracania z bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="ba6a4-107">To polecenie cmdlet jest obecnie obsługiwane przez usługę hurtowni danych programu SQL Server w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="ba6a4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba6a4-108">EXAMPLES</span></span>

### <span data-ttu-id="ba6a4-109">Przykład 1. usuwa punkt przywracania</span><span class="sxs-lookup"><span data-stu-id="ba6a4-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="ba6a4-110">To polecenie usuwa punkt przywracania bazy danych SQL Azure o danej dacie utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="ba6a4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba6a4-111">PARAMETERS</span></span>

### <span data-ttu-id="ba6a4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba6a4-112">-DatabaseName</span></span>
<span data-ttu-id="ba6a4-113">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ba6a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6a4-114">-DefaultProfile</span></span>
<span data-ttu-id="ba6a4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ba6a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba6a4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6a4-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba6a4-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ba6a4-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="ba6a4-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="ba6a4-119">Określa datę utworzenia punktu przywracania.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6a4-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba6a4-120">-ServerName</span></span>
<span data-ttu-id="ba6a4-121">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ba6a4-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba6a4-122">-Confirm</span></span>
<span data-ttu-id="ba6a4-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6a4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6a4-124">-WhatIf</span></span>
<span data-ttu-id="ba6a4-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6a4-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6a4-127">CommonParameters</span></span>
<span data-ttu-id="ba6a4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6a4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba6a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6a4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba6a4-130">INPUTS</span></span>

## <span data-ttu-id="ba6a4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba6a4-131">OUTPUTS</span></span>

## <span data-ttu-id="ba6a4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba6a4-132">NOTES</span></span>

## <span data-ttu-id="ba6a4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba6a4-133">RELATED LINKS</span></span>
