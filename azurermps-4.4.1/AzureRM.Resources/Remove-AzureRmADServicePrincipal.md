---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718096"
---
# <span data-ttu-id="5e972-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e972-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="5e972-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e972-102">SYNOPSIS</span></span>
<span data-ttu-id="5e972-103">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e972-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e972-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e972-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e972-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e972-105">DESCRIPTION</span></span>
<span data-ttu-id="5e972-106">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e972-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="5e972-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e972-107">EXAMPLES</span></span>

### <span data-ttu-id="5e972-108">--------------------------Usunąć podmiot zabezpieczeń usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="5e972-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="5e972-109">Usuwa dane główne usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e972-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="5e972-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e972-110">PARAMETERS</span></span>

### <span data-ttu-id="5e972-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5e972-111">-Force</span></span>
<span data-ttu-id="5e972-112">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="5e972-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="5e972-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5e972-113">-ObjectId</span></span>
<span data-ttu-id="5e972-114">Identyfikator obiektu podmiotu usługi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5e972-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e972-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e972-115">-PassThru</span></span>
<span data-ttu-id="5e972-116">Jeśli ta funkcja jest określona, zwraca usunięty podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="5e972-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="5e972-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e972-117">-Confirm</span></span>
<span data-ttu-id="5e972-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e972-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e972-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e972-119">-WhatIf</span></span>
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

### <span data-ttu-id="5e972-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e972-120">-DefaultProfile</span></span>
<span data-ttu-id="5e972-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e972-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e972-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e972-122">CommonParameters</span></span>
<span data-ttu-id="5e972-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e972-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e972-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e972-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e972-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e972-125">INPUTS</span></span>

## <span data-ttu-id="5e972-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e972-126">OUTPUTS</span></span>

### <span data-ttu-id="5e972-127">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e972-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="5e972-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e972-128">NOTES</span></span>
<span data-ttu-id="5e972-129">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="5e972-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5e972-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e972-130">RELATED LINKS</span></span>

[<span data-ttu-id="5e972-131">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e972-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5e972-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e972-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5e972-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e972-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5e972-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5e972-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="5e972-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e972-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
