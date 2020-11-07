---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524538"
---
# <span data-ttu-id="f55b0-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f55b0-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="f55b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f55b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f55b0-103">Odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="f55b0-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f55b0-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f55b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f55b0-106">Polecenie cmdlet **REVOKE-AzureRmSnapshotAccess** odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="f55b0-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="f55b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f55b0-107">EXAMPLES</span></span>

### <span data-ttu-id="f55b0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f55b0-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="f55b0-109">Odwoływanie dostępu do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="f55b0-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="f55b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f55b0-110">PARAMETERS</span></span>

### <span data-ttu-id="f55b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f55b0-111">-AsJob</span></span>
<span data-ttu-id="f55b0-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f55b0-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55b0-113">-DefaultProfile</span></span>
<span data-ttu-id="f55b0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f55b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="f55b0-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f55b0-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f55b0-117">-SnapshotName</span></span>
<span data-ttu-id="f55b0-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="f55b0-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f55b0-119">-Confirm</span></span>
<span data-ttu-id="f55b0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55b0-121">-WhatIf</span></span>
<span data-ttu-id="f55b0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55b0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f55b0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f55b0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55b0-124">CommonParameters</span></span>
<span data-ttu-id="f55b0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55b0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55b0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f55b0-127">INPUTS</span></span>

### <span data-ttu-id="f55b0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f55b0-128">System.String</span></span>

## <span data-ttu-id="f55b0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f55b0-129">OUTPUTS</span></span>

### <span data-ttu-id="f55b0-130">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f55b0-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f55b0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f55b0-131">NOTES</span></span>

## <span data-ttu-id="f55b0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f55b0-132">RELATED LINKS</span></span>