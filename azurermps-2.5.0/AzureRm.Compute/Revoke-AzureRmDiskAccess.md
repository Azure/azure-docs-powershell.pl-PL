---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898037"
---
# <span data-ttu-id="4b64a-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4b64a-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="4b64a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b64a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b64a-103">Odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="4b64a-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b64a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b64a-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b64a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b64a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b64a-106">Polecenie cmdlet **REVOKE-AzureRmDiskAccess** odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="4b64a-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="4b64a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b64a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b64a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b64a-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="4b64a-109">Odwoływanie dostępu do dysku o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="4b64a-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="4b64a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b64a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b64a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b64a-111">-AsJob</span></span>
<span data-ttu-id="4b64a-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4b64a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b64a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b64a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b64a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b64a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b64a-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="4b64a-115">-DiskName</span></span>
<span data-ttu-id="4b64a-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="4b64a-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b64a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b64a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b64a-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4b64a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b64a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b64a-119">-Confirm</span></span>
<span data-ttu-id="4b64a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b64a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b64a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b64a-121">-WhatIf</span></span>
<span data-ttu-id="4b64a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b64a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b64a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b64a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b64a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b64a-124">CommonParameters</span></span>
<span data-ttu-id="4b64a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b64a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b64a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b64a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b64a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b64a-127">INPUTS</span></span>

### <span data-ttu-id="4b64a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b64a-128">System.String</span></span>

## <span data-ttu-id="4b64a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b64a-129">OUTPUTS</span></span>

### <span data-ttu-id="4b64a-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="4b64a-130">System.Object</span></span>

## <span data-ttu-id="4b64a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b64a-131">NOTES</span></span>

## <span data-ttu-id="4b64a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b64a-132">RELATED LINKS</span></span>

