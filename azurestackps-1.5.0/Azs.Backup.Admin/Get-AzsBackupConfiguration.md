---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523734"
---
# <span data-ttu-id="7a5a9-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a5a9-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="7a5a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5a9-103">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="7a5a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a5a9-104">SYNTAX</span></span>

### <span data-ttu-id="7a5a9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7a5a9-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7a5a9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7a5a9-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7a5a9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="7a5a9-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7a5a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a5a9-108">DESCRIPTION</span></span>
<span data-ttu-id="7a5a9-109">Zwraca listę konfiguracji kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="7a5a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a5a9-110">EXAMPLES</span></span>

### <span data-ttu-id="7a5a9-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a5a9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="7a5a9-112">Pobierz konfigurację kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="7a5a9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a5a9-113">PARAMETERS</span></span>

### <span data-ttu-id="7a5a9-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7a5a9-114">-Location</span></span>
<span data-ttu-id="7a5a9-115">Lokalizacja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-115">Backup location.</span></span>

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

### <span data-ttu-id="7a5a9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5a9-116">-ResourceGroupName</span></span>
<span data-ttu-id="7a5a9-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="7a5a9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a5a9-118">-ResourceId</span></span>
<span data-ttu-id="7a5a9-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-119">The resource id.</span></span>

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

### <span data-ttu-id="7a5a9-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="7a5a9-120">-Skip</span></span>
<span data-ttu-id="7a5a9-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7a5a9-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="7a5a9-122">-Top</span></span>
<span data-ttu-id="7a5a9-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7a5a9-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7a5a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5a9-125">CommonParameters</span></span>
<span data-ttu-id="7a5a9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5a9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a5a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5a9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a5a9-128">INPUTS</span></span>

## <span data-ttu-id="7a5a9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a5a9-129">OUTPUTS</span></span>

### <span data-ttu-id="7a5a9-130">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="7a5a9-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="7a5a9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a5a9-131">NOTES</span></span>

## <span data-ttu-id="7a5a9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a5a9-132">RELATED LINKS</span></span>

