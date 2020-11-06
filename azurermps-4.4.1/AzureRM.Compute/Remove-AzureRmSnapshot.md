---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553968"
---
# <span data-ttu-id="af523-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="af523-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="af523-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af523-102">SYNOPSIS</span></span>
<span data-ttu-id="af523-103">Usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="af523-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af523-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af523-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af523-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af523-105">DESCRIPTION</span></span>
<span data-ttu-id="af523-106">Polecenie cmdlet **Remove-AzureRmSnapshot** umożliwia usunięcie migawki.</span><span class="sxs-lookup"><span data-stu-id="af523-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="af523-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af523-107">EXAMPLES</span></span>

### <span data-ttu-id="af523-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af523-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="af523-109">To polecenie usuwa migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="af523-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="af523-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af523-110">PARAMETERS</span></span>

### <span data-ttu-id="af523-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af523-111">-DefaultProfile</span></span>
<span data-ttu-id="af523-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af523-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af523-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af523-113">-Force</span></span>
<span data-ttu-id="af523-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af523-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af523-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af523-115">-ResourceGroupName</span></span>
<span data-ttu-id="af523-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af523-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af523-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="af523-117">-SnapshotName</span></span>
<span data-ttu-id="af523-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="af523-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="af523-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af523-119">-Confirm</span></span>
<span data-ttu-id="af523-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af523-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af523-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af523-121">-WhatIf</span></span>
<span data-ttu-id="af523-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af523-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af523-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af523-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af523-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af523-124">CommonParameters</span></span>
<span data-ttu-id="af523-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af523-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af523-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af523-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af523-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af523-127">INPUTS</span></span>

### <span data-ttu-id="af523-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af523-128">System.String</span></span>

## <span data-ttu-id="af523-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af523-129">OUTPUTS</span></span>

### <span data-ttu-id="af523-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="af523-130">System.Object</span></span>

## <span data-ttu-id="af523-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af523-131">NOTES</span></span>

## <span data-ttu-id="af523-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af523-132">RELATED LINKS</span></span>

