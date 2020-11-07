---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719634"
---
# <span data-ttu-id="fb530-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fb530-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="fb530-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb530-102">SYNOPSIS</span></span>
<span data-ttu-id="fb530-103">Usuwa konto integracji.</span><span class="sxs-lookup"><span data-stu-id="fb530-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb530-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb530-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb530-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb530-105">DESCRIPTION</span></span>
<span data-ttu-id="fb530-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccount** umożliwia usunięcie konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb530-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="fb530-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb530-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="fb530-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="fb530-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fb530-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fb530-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fb530-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="fb530-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fb530-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="fb530-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fb530-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb530-112">EXAMPLES</span></span>

### <span data-ttu-id="fb530-113">Przykład 1: usuwanie konta integracji</span><span class="sxs-lookup"><span data-stu-id="fb530-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="fb530-114">To polecenie usuwa konto integracyjne o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="fb530-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="fb530-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb530-115">PARAMETERS</span></span>

### <span data-ttu-id="fb530-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fb530-116">-Force</span></span>
<span data-ttu-id="fb530-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb530-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb530-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb530-118">-Name</span></span>
<span data-ttu-id="fb530-119">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fb530-119">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb530-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb530-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb530-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb530-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb530-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb530-122">-Confirm</span></span>
<span data-ttu-id="fb530-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb530-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb530-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb530-124">-WhatIf</span></span>
<span data-ttu-id="fb530-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb530-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb530-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb530-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb530-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb530-127">-DefaultProfile</span></span>
<span data-ttu-id="fb530-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb530-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb530-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb530-129">CommonParameters</span></span>
<span data-ttu-id="fb530-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb530-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb530-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb530-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb530-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb530-132">INPUTS</span></span>

## <span data-ttu-id="fb530-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb530-133">OUTPUTS</span></span>

## <span data-ttu-id="fb530-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb530-134">NOTES</span></span>

## <span data-ttu-id="fb530-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb530-135">RELATED LINKS</span></span>

[<span data-ttu-id="fb530-136">Nowe — AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fb530-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="fb530-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fb530-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="fb530-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fb530-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


