---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717695"
---
# <span data-ttu-id="44790-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="44790-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="44790-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44790-102">SYNOPSIS</span></span>
<span data-ttu-id="44790-103">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="44790-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44790-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44790-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44790-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44790-105">DESCRIPTION</span></span>
<span data-ttu-id="44790-106">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="44790-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="44790-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44790-107">EXAMPLES</span></span>

### <span data-ttu-id="44790-108">Usuń aplikację AAD.</span><span class="sxs-lookup"><span data-stu-id="44790-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="44790-109">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="44790-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="44790-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44790-110">PARAMETERS</span></span>

### <span data-ttu-id="44790-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44790-111">-DefaultProfile</span></span>
<span data-ttu-id="44790-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="44790-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44790-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44790-113">-Force</span></span>
<span data-ttu-id="44790-114">Przełączanie w celu usunięcia aplikacji bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="44790-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="44790-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="44790-115">-ObjectId</span></span>
<span data-ttu-id="44790-116">Identyfikator obiektu aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="44790-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44790-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44790-117">-Confirm</span></span>
<span data-ttu-id="44790-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44790-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44790-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44790-119">-WhatIf</span></span>
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

### <span data-ttu-id="44790-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44790-120">CommonParameters</span></span>
<span data-ttu-id="44790-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44790-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44790-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44790-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44790-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44790-123">INPUTS</span></span>

### <span data-ttu-id="44790-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="44790-124">None</span></span>
<span data-ttu-id="44790-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="44790-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44790-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44790-126">OUTPUTS</span></span>

## <span data-ttu-id="44790-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44790-127">NOTES</span></span>
<span data-ttu-id="44790-128">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="44790-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="44790-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44790-129">RELATED LINKS</span></span>

[<span data-ttu-id="44790-130">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="44790-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="44790-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="44790-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="44790-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="44790-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="44790-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="44790-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

