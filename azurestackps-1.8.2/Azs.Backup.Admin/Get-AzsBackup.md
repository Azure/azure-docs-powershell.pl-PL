---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055568"
---
# <span data-ttu-id="3d326-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="3d326-101">Get-AzsBackup</span></span>

## <span data-ttu-id="3d326-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d326-102">SYNOPSIS</span></span>
<span data-ttu-id="3d326-103">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="3d326-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="3d326-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d326-104">SYNTAX</span></span>

### <span data-ttu-id="3d326-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d326-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d326-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3d326-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d326-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3d326-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="3d326-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="3d326-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3d326-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3d326-109">DESCRIPTION</span></span>
<span data-ttu-id="3d326-110">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="3d326-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="3d326-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d326-111">EXAMPLES</span></span>

### <span data-ttu-id="3d326-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3d326-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="3d326-113">Pobierz informacje sbout wszystkie kopie zapasowe stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d326-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="3d326-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3d326-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="3d326-115">Uzyskiwanie informacji na temat określonej kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d326-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="3d326-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d326-116">PARAMETERS</span></span>

### <span data-ttu-id="3d326-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3d326-117">-Location</span></span>
<span data-ttu-id="3d326-118">Lokalizacja z kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="3d326-118">Location backed up.</span></span>

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

### <span data-ttu-id="3d326-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d326-119">-Name</span></span>
<span data-ttu-id="3d326-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3d326-120">Name of the backup.</span></span>

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

### <span data-ttu-id="3d326-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="3d326-121">-ParentResource</span></span>
<span data-ttu-id="3d326-122">Przekazanie lokalizacji kopii zapasowej spowoduje zwrócenie listy wszystkich kopii zapasowych w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3d326-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="3d326-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d326-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d326-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d326-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="3d326-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d326-125">-ResourceId</span></span>
<span data-ttu-id="3d326-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d326-126">The resource id.</span></span>

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

### <span data-ttu-id="3d326-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="3d326-127">-Skip</span></span>
<span data-ttu-id="3d326-128">{{Opis pomijania wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="3d326-128">{{Fill Skip Description}}</span></span>

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

### <span data-ttu-id="3d326-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="3d326-129">-Top</span></span>
<span data-ttu-id="3d326-130">{{Opis na wypełnieniu}}</span><span class="sxs-lookup"><span data-stu-id="3d326-130">{{Fill Top Description}}</span></span>

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

### <span data-ttu-id="3d326-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d326-131">CommonParameters</span></span>
<span data-ttu-id="3d326-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d326-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d326-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d326-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d326-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d326-134">INPUTS</span></span>

## <span data-ttu-id="3d326-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d326-135">OUTPUTS</span></span>

### <span data-ttu-id="3d326-136">Microsoft. AzureStack. Management. Backup. admin. models. Backup</span><span class="sxs-lookup"><span data-stu-id="3d326-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="3d326-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d326-137">NOTES</span></span>

## <span data-ttu-id="3d326-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d326-138">RELATED LINKS</span></span>

