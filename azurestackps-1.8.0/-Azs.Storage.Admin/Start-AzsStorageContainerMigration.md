---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889070"
---
# <span data-ttu-id="a3400-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="a3400-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="a3400-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3400-102">SYNOPSIS</span></span>
<span data-ttu-id="a3400-103">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="a3400-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="a3400-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3400-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3400-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3400-105">DESCRIPTION</span></span>
<span data-ttu-id="a3400-106">Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="a3400-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="a3400-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3400-107">EXAMPLES</span></span>

### <span data-ttu-id="a3400-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a3400-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="a3400-109">Rozpoczynanie migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="a3400-109">Starts a container migration.</span></span>

## <span data-ttu-id="a3400-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3400-110">PARAMETERS</span></span>

### <span data-ttu-id="a3400-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3400-111">-AsJob</span></span>
<span data-ttu-id="a3400-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="a3400-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a3400-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="a3400-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="a3400-114">Ścieżka UNC udziału docelowego do migracji.</span><span class="sxs-lookup"><span data-stu-id="a3400-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="a3400-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a3400-115">-FarmName</span></span>
<span data-ttu-id="a3400-116">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="a3400-116">Farm Id.</span></span>

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

### <span data-ttu-id="a3400-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3400-117">-Force</span></span>
<span data-ttu-id="a3400-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3400-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3400-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3400-119">-Name</span></span>
<span data-ttu-id="a3400-120">Nazwa kontenera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="a3400-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3400-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3400-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3400-122">Nazwa grupy zasobów, w której zarejestrowano dostawcę zasobów magazynu.</span><span class="sxs-lookup"><span data-stu-id="a3400-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="a3400-123">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="a3400-123">-ShareName</span></span>
<span data-ttu-id="a3400-124">Nazwa udziału zawierającego kontener określony do migracji.</span><span class="sxs-lookup"><span data-stu-id="a3400-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="a3400-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a3400-125">-StorageAccountName</span></span>
<span data-ttu-id="a3400-126">Nazwa konta magazynu, w którym znajduje się kontener.</span><span class="sxs-lookup"><span data-stu-id="a3400-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="a3400-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3400-127">-Confirm</span></span>
<span data-ttu-id="a3400-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3400-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3400-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3400-129">-WhatIf</span></span>
<span data-ttu-id="a3400-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3400-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3400-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3400-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3400-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3400-132">CommonParameters</span></span>
<span data-ttu-id="a3400-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3400-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3400-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3400-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3400-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3400-135">INPUTS</span></span>

## <span data-ttu-id="a3400-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3400-136">OUTPUTS</span></span>

## <span data-ttu-id="a3400-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3400-137">NOTES</span></span>

## <span data-ttu-id="a3400-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3400-138">RELATED LINKS</span></span>

