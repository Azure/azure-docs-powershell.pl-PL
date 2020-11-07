---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889754"
---
# <span data-ttu-id="81078-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="81078-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="81078-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81078-102">SYNOPSIS</span></span>
<span data-ttu-id="81078-103">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="81078-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="81078-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81078-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81078-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81078-105">DESCRIPTION</span></span>
<span data-ttu-id="81078-106">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="81078-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="81078-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81078-107">EXAMPLES</span></span>

### <span data-ttu-id="81078-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="81078-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="81078-109">Rozpoczynanie migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="81078-109">Starts a container migration.</span></span>

## <span data-ttu-id="81078-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81078-110">PARAMETERS</span></span>

### <span data-ttu-id="81078-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81078-111">-StorageAccountName</span></span>
<span data-ttu-id="81078-112">Nazwa konta magazynu, w którym znajduje się kontener.</span><span class="sxs-lookup"><span data-stu-id="81078-112">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="81078-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="81078-113">-ContainerName</span></span>
<span data-ttu-id="81078-114">Nazwa kontenera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="81078-114">The name of the container to be migrated.</span></span>

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

### <span data-ttu-id="81078-115">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="81078-115">-ShareName</span></span>
<span data-ttu-id="81078-116">Nazwa udziału zawierającego kontener określony do migracji.</span><span class="sxs-lookup"><span data-stu-id="81078-116">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="81078-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81078-117">-ResourceGroupName</span></span>
<span data-ttu-id="81078-118">Nazwa grupy zasobów, w której zarejestrowano dostawcę zasobów magazynu.</span><span class="sxs-lookup"><span data-stu-id="81078-118">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="81078-119">-Farmname</span><span class="sxs-lookup"><span data-stu-id="81078-119">-FarmName</span></span>
<span data-ttu-id="81078-120">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="81078-120">Farm Id.</span></span>

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

### <span data-ttu-id="81078-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="81078-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="81078-122">Ścieżka UNC udziału docelowego do migracji.</span><span class="sxs-lookup"><span data-stu-id="81078-122">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="81078-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81078-123">-AsJob</span></span>
<span data-ttu-id="81078-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="81078-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="81078-125">-Force</span><span class="sxs-lookup"><span data-stu-id="81078-125">-Force</span></span>
<span data-ttu-id="81078-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81078-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="81078-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81078-127">-WhatIf</span></span>
<span data-ttu-id="81078-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81078-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81078-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81078-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81078-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81078-130">-Confirm</span></span>
<span data-ttu-id="81078-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81078-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81078-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81078-132">CommonParameters</span></span>
<span data-ttu-id="81078-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81078-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81078-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81078-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81078-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81078-135">INPUTS</span></span>

## <span data-ttu-id="81078-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81078-136">OUTPUTS</span></span>

## <span data-ttu-id="81078-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81078-137">NOTES</span></span>

## <span data-ttu-id="81078-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81078-138">RELATED LINKS</span></span>
