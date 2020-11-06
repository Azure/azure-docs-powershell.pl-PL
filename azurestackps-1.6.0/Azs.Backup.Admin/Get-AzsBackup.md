---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523938"
---
# <span data-ttu-id="89b86-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="89b86-101">Get-AzsBackup</span></span>

## <span data-ttu-id="89b86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89b86-102">SYNOPSIS</span></span>
<span data-ttu-id="89b86-103">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="89b86-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="89b86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89b86-104">SYNTAX</span></span>

### <span data-ttu-id="89b86-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="89b86-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="89b86-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="89b86-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b86-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="89b86-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="89b86-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="89b86-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="89b86-109">Opis</span><span class="sxs-lookup"><span data-stu-id="89b86-109">DESCRIPTION</span></span>
<span data-ttu-id="89b86-110">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="89b86-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="89b86-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89b86-111">EXAMPLES</span></span>

### <span data-ttu-id="89b86-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="89b86-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="89b86-113">Uzyskaj informacje na temat wszystkich kopii zapasowych stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89b86-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="89b86-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="89b86-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="89b86-115">Uzyskiwanie informacji o określonej kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89b86-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="89b86-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89b86-116">PARAMETERS</span></span>

### <span data-ttu-id="89b86-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="89b86-117">-Location</span></span>
<span data-ttu-id="89b86-118">Lokalizacja z kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="89b86-118">Location backed up.</span></span>

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

### <span data-ttu-id="89b86-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89b86-119">-Name</span></span>
<span data-ttu-id="89b86-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="89b86-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b86-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="89b86-121">-ParentResource</span></span>
<span data-ttu-id="89b86-122">Przekazanie lokalizacji kopii zapasowej spowoduje zwrócenie listy wszystkich kopii zapasowych w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="89b86-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b86-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b86-123">-ResourceGroupName</span></span>
<span data-ttu-id="89b86-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89b86-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="89b86-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89b86-125">-ResourceId</span></span>
<span data-ttu-id="89b86-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="89b86-126">The resource id.</span></span>

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

### <span data-ttu-id="89b86-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="89b86-127">-Skip</span></span>
<span data-ttu-id="89b86-128">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="89b86-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b86-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="89b86-129">-Top</span></span>
<span data-ttu-id="89b86-130">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="89b86-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="89b86-131">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="89b86-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b86-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b86-132">CommonParameters</span></span>
<span data-ttu-id="89b86-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b86-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b86-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b86-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b86-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89b86-135">INPUTS</span></span>

## <span data-ttu-id="89b86-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89b86-136">OUTPUTS</span></span>

### <span data-ttu-id="89b86-137">Microsoft. AzureStack. Management. Backup. admin. models. Backup</span><span class="sxs-lookup"><span data-stu-id="89b86-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="89b86-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89b86-138">NOTES</span></span>

## <span data-ttu-id="89b86-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89b86-139">RELATED LINKS</span></span>

