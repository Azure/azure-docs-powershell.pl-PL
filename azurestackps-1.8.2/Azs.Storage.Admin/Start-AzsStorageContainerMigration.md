---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061524"
---
# <span data-ttu-id="d9560-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="d9560-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="d9560-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9560-102">SYNOPSIS</span></span>
<span data-ttu-id="d9560-103">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="d9560-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="d9560-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9560-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9560-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9560-105">DESCRIPTION</span></span>
<span data-ttu-id="d9560-106">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="d9560-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="d9560-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9560-107">EXAMPLES</span></span>

### <span data-ttu-id="d9560-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="d9560-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="d9560-109">Rozpoczynanie migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="d9560-109">Starts a container migration.</span></span>

## <span data-ttu-id="d9560-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9560-110">PARAMETERS</span></span>

### <span data-ttu-id="d9560-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9560-111">-StorageAccountName</span></span>
<span data-ttu-id="d9560-112">Nazwa konta magazynu, w którym znajduje się kontener.</span><span class="sxs-lookup"><span data-stu-id="d9560-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d9560-113">-ContainerName</span></span>
<span data-ttu-id="d9560-114">Nazwa kontenera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="d9560-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-115">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="d9560-115">-ShareName</span></span>
<span data-ttu-id="d9560-116">Nazwa udziału zawierającego kontener określony do migracji.</span><span class="sxs-lookup"><span data-stu-id="d9560-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9560-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9560-118">Nazwa grupy zasobów, w której zarejestrowano dostawcę zasobów magazynu.</span><span class="sxs-lookup"><span data-stu-id="d9560-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-119">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d9560-119">-FarmName</span></span>
<span data-ttu-id="d9560-120">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="d9560-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="d9560-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="d9560-122">Ścieżka UNC udziału docelowego do migracji.</span><span class="sxs-lookup"><span data-stu-id="d9560-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9560-123">-AsJob</span></span>
<span data-ttu-id="d9560-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="d9560-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d9560-125">-Force</span></span>
<span data-ttu-id="d9560-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9560-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9560-127">-WhatIf</span></span>
<span data-ttu-id="d9560-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9560-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9560-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9560-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9560-130">-Confirm</span></span>
<span data-ttu-id="d9560-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9560-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9560-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9560-132">CommonParameters</span></span>
<span data-ttu-id="d9560-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9560-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9560-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9560-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9560-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9560-135">INPUTS</span></span>

## <span data-ttu-id="d9560-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9560-136">OUTPUTS</span></span>

## <span data-ttu-id="d9560-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9560-137">NOTES</span></span>

## <span data-ttu-id="d9560-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9560-138">RELATED LINKS</span></span>
