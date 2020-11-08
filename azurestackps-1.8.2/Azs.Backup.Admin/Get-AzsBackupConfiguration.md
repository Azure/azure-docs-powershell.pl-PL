---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055607"
---
# <span data-ttu-id="1b417-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b417-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="1b417-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b417-102">SYNOPSIS</span></span>
<span data-ttu-id="1b417-103">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="1b417-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1b417-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b417-104">SYNTAX</span></span>

### <span data-ttu-id="1b417-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1b417-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1b417-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1b417-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1b417-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1b417-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1b417-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1b417-108">DESCRIPTION</span></span>
<span data-ttu-id="1b417-109">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="1b417-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1b417-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b417-110">EXAMPLES</span></span>

### <span data-ttu-id="1b417-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1b417-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="1b417-112">Pobierz konfigurację kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="1b417-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="1b417-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b417-113">PARAMETERS</span></span>

### <span data-ttu-id="1b417-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b417-114">-Location</span></span>
<span data-ttu-id="1b417-115">Lokalizacja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1b417-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b417-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b417-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b417-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b417-117">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b417-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b417-118">-ResourceId</span></span>
<span data-ttu-id="1b417-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1b417-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b417-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="1b417-120">-Skip</span></span>
<span data-ttu-id="1b417-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1b417-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b417-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="1b417-122">-Top</span></span>
<span data-ttu-id="1b417-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1b417-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1b417-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="1b417-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b417-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b417-125">CommonParameters</span></span>
<span data-ttu-id="1b417-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b417-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b417-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b417-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b417-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b417-128">INPUTS</span></span>

## <span data-ttu-id="1b417-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b417-129">OUTPUTS</span></span>

### <span data-ttu-id="1b417-130">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="1b417-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="1b417-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b417-131">NOTES</span></span>

## <span data-ttu-id="1b417-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b417-132">RELATED LINKS</span></span>

