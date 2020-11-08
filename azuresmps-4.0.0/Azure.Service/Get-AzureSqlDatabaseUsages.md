---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055529"
---
# <span data-ttu-id="a03fe-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="a03fe-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="a03fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a03fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a03fe-103">Pobiera limit rozmiaru i rozmiaru bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a03fe-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="a03fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a03fe-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a03fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a03fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a03fe-106">Polecenie cmdlet **Get-AzureSqlDatabaseUsages** Pobiera bieżący rozmiar i limit rozmiaru bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a03fe-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="a03fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a03fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a03fe-108">Przykład 1: uzyskiwanie informacji o użyciu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a03fe-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a03fe-109">To polecenie uzyskuje informacje o limicie rozmiaru i rozmiarze bazy danych SQL o nazwie Database01 na server01.</span><span class="sxs-lookup"><span data-stu-id="a03fe-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="a03fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a03fe-110">PARAMETERS</span></span>

### <span data-ttu-id="a03fe-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a03fe-111">-DatabaseName</span></span>
<span data-ttu-id="a03fe-112">Określa nazwę bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a03fe-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03fe-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a03fe-113">-Profile</span></span>
<span data-ttu-id="a03fe-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a03fe-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a03fe-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a03fe-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03fe-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a03fe-116">-ServerName</span></span>
<span data-ttu-id="a03fe-117">Określa nazwę serwera obsługującego bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a03fe-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03fe-118">CommonParameters</span></span>
<span data-ttu-id="a03fe-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03fe-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03fe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03fe-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a03fe-121">INPUTS</span></span>

## <span data-ttu-id="a03fe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a03fe-122">OUTPUTS</span></span>

## <span data-ttu-id="a03fe-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a03fe-123">NOTES</span></span>

## <span data-ttu-id="a03fe-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a03fe-124">RELATED LINKS</span></span>

