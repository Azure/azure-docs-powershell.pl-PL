---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889330"
---
# <span data-ttu-id="e4ca4-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4ca4-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="e4ca4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ca4-103">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e4ca4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4ca4-104">SYNTAX</span></span>

### <span data-ttu-id="e4ca4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e4ca4-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e4ca4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e4ca4-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e4ca4-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e4ca4-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e4ca4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4ca4-108">DESCRIPTION</span></span>
<span data-ttu-id="e4ca4-109">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e4ca4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4ca4-110">EXAMPLES</span></span>

### <span data-ttu-id="e4ca4-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4ca4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="e4ca4-112">Pobierz konfigurację kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="e4ca4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4ca4-113">PARAMETERS</span></span>

### <span data-ttu-id="e4ca4-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4ca4-114">-Location</span></span>
<span data-ttu-id="e4ca4-115">Lokalizacja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-115">Backup location.</span></span>

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

### <span data-ttu-id="e4ca4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4ca4-116">-ResourceGroupName</span></span>
<span data-ttu-id="e4ca4-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="e4ca4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4ca4-118">-ResourceId</span></span>
<span data-ttu-id="e4ca4-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-119">The resource id.</span></span>

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

### <span data-ttu-id="e4ca4-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="e4ca4-120">-Skip</span></span>
<span data-ttu-id="e4ca4-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e4ca4-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="e4ca4-122">-Top</span></span>
<span data-ttu-id="e4ca4-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e4ca4-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e4ca4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ca4-125">CommonParameters</span></span>
<span data-ttu-id="e4ca4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ca4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ca4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ca4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ca4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4ca4-128">INPUTS</span></span>

## <span data-ttu-id="e4ca4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4ca4-129">OUTPUTS</span></span>

### <span data-ttu-id="e4ca4-130">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="e4ca4-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="e4ca4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4ca4-131">NOTES</span></span>

## <span data-ttu-id="e4ca4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4ca4-132">RELATED LINKS</span></span>

