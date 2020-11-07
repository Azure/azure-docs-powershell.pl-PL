---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889814"
---
# <span data-ttu-id="58c14-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="58c14-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="58c14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58c14-102">SYNOPSIS</span></span>
<span data-ttu-id="58c14-103">Zwraca stan zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="58c14-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="58c14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58c14-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="58c14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58c14-105">DESCRIPTION</span></span>
<span data-ttu-id="58c14-106">Zwraca stan zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="58c14-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="58c14-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58c14-107">EXAMPLES</span></span>

### <span data-ttu-id="58c14-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="58c14-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="58c14-109">Uzyskiwanie stanu zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="58c14-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="58c14-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58c14-110">PARAMETERS</span></span>

### <span data-ttu-id="58c14-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="58c14-111">-FarmName</span></span>
<span data-ttu-id="58c14-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="58c14-112">Farm Id.</span></span>

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

### <span data-ttu-id="58c14-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="58c14-113">-JobId</span></span>
<span data-ttu-id="58c14-114">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="58c14-114">Operation Id.</span></span>

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

### <span data-ttu-id="58c14-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c14-115">-ResourceGroupName</span></span>
<span data-ttu-id="58c14-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58c14-116">Resource group name.</span></span>

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

### <span data-ttu-id="58c14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c14-117">CommonParameters</span></span>
<span data-ttu-id="58c14-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c14-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c14-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c14-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58c14-120">INPUTS</span></span>

## <span data-ttu-id="58c14-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58c14-121">OUTPUTS</span></span>

### <span data-ttu-id="58c14-122">Microsoft. AzureStack. Management. Storage. admin. models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="58c14-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="58c14-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58c14-123">NOTES</span></span>

## <span data-ttu-id="58c14-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58c14-124">RELATED LINKS</span></span>
