---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545963"
---
# <span data-ttu-id="6b204-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b204-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="6b204-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b204-102">SYNOPSIS</span></span>
<span data-ttu-id="6b204-103">Ustawia zasady przechowywania długoterminowych serwerów.</span><span class="sxs-lookup"><span data-stu-id="6b204-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b204-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b204-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b204-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b204-105">DESCRIPTION</span></span>
<span data-ttu-id="6b204-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** ustawia zasady przechowywania terminów długoterminowych zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="6b204-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="6b204-107">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="6b204-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="6b204-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b204-108">EXAMPLES</span></span>

## <span data-ttu-id="6b204-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b204-109">PARAMETERS</span></span>

### <span data-ttu-id="6b204-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b204-110">-DatabaseName</span></span>
<span data-ttu-id="6b204-111">Określa nazwę bazy danych SQL, dla której to polecenie cmdlet ustawia zasady.</span><span class="sxs-lookup"><span data-stu-id="6b204-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="6b204-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b204-112">-ResourceGroupName</span></span>
<span data-ttu-id="6b204-113">Określa nazwę grupy zasobów zawierającej bazę danych.</span><span class="sxs-lookup"><span data-stu-id="6b204-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="6b204-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b204-114">-ResourceId</span></span>
<span data-ttu-id="6b204-115">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b204-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b204-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6b204-116">-ServerName</span></span>
<span data-ttu-id="6b204-117">Określa serwer, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="6b204-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="6b204-118">-State</span><span class="sxs-lookup"><span data-stu-id="6b204-118">-State</span></span>
<span data-ttu-id="6b204-119">Określa stan.</span><span class="sxs-lookup"><span data-stu-id="6b204-119">Specifies a state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b204-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b204-120">-Confirm</span></span>
<span data-ttu-id="6b204-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b204-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b204-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b204-122">-WhatIf</span></span>
<span data-ttu-id="6b204-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b204-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b204-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b204-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b204-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b204-125">-DefaultProfile</span></span>
<span data-ttu-id="6b204-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b204-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b204-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b204-127">CommonParameters</span></span>
<span data-ttu-id="6b204-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b204-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b204-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b204-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b204-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b204-130">INPUTS</span></span>

## <span data-ttu-id="6b204-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b204-131">OUTPUTS</span></span>

## <span data-ttu-id="6b204-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b204-132">NOTES</span></span>

## <span data-ttu-id="6b204-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b204-133">RELATED LINKS</span></span>

[<span data-ttu-id="6b204-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b204-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6b204-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6b204-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
