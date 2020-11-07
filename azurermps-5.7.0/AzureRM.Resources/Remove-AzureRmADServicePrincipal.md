---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717692"
---
# <span data-ttu-id="b9352-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9352-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b9352-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9352-102">SYNOPSIS</span></span>
<span data-ttu-id="b9352-103">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9352-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9352-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9352-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9352-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9352-105">DESCRIPTION</span></span>
<span data-ttu-id="b9352-106">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9352-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="b9352-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9352-107">EXAMPLES</span></span>

### <span data-ttu-id="b9352-108">Usuń podmiot zabezpieczeń usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="b9352-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="b9352-109">Usuwa dane główne usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9352-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="b9352-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9352-110">PARAMETERS</span></span>

### <span data-ttu-id="b9352-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9352-111">-DefaultProfile</span></span>
<span data-ttu-id="b9352-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9352-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9352-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b9352-113">-Force</span></span>
<span data-ttu-id="b9352-114">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="b9352-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="b9352-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b9352-115">-ObjectId</span></span>
<span data-ttu-id="b9352-116">Identyfikator obiektu podmiotu usługi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b9352-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9352-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9352-117">-PassThru</span></span>
<span data-ttu-id="b9352-118">Jeśli ta funkcja jest określona, zwraca usunięty podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b9352-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="b9352-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9352-119">-Confirm</span></span>
<span data-ttu-id="b9352-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9352-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9352-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9352-121">-WhatIf</span></span>
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

### <span data-ttu-id="b9352-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9352-122">CommonParameters</span></span>
<span data-ttu-id="b9352-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9352-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9352-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9352-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9352-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9352-125">INPUTS</span></span>

### <span data-ttu-id="b9352-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9352-126">None</span></span>
<span data-ttu-id="b9352-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b9352-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9352-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9352-128">OUTPUTS</span></span>

### <span data-ttu-id="b9352-129">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9352-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b9352-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9352-130">NOTES</span></span>
<span data-ttu-id="b9352-131">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="b9352-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b9352-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9352-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9352-133">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9352-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9352-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9352-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9352-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9352-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9352-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b9352-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b9352-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b9352-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
