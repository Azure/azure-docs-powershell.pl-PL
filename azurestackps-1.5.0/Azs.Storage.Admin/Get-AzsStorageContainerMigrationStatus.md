---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710712"
---
# <span data-ttu-id="7c5cf-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="7c5cf-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="7c5cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5cf-103">Zwraca stan zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="7c5cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c5cf-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c5cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c5cf-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5cf-106">Zwraca stan zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="7c5cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c5cf-107">EXAMPLES</span></span>

### <span data-ttu-id="7c5cf-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c5cf-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="7c5cf-109">Uzyskiwanie stanu zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="7c5cf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c5cf-110">PARAMETERS</span></span>

### <span data-ttu-id="7c5cf-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7c5cf-111">-FarmName</span></span>
<span data-ttu-id="7c5cf-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-112">Farm Id.</span></span>

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

### <span data-ttu-id="7c5cf-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="7c5cf-113">-JobId</span></span>
<span data-ttu-id="7c5cf-114">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c5cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="7c5cf-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c5cf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5cf-117">CommonParameters</span></span>
<span data-ttu-id="7c5cf-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5cf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5cf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c5cf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5cf-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c5cf-120">INPUTS</span></span>

## <span data-ttu-id="7c5cf-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c5cf-121">OUTPUTS</span></span>

### <span data-ttu-id="7c5cf-122">Microsoft. AzureStack. Management. Storage. admin. models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="7c5cf-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="7c5cf-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c5cf-123">NOTES</span></span>

## <span data-ttu-id="7c5cf-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c5cf-124">RELATED LINKS</span></span>

