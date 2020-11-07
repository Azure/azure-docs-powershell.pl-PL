---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 7342601bba3c963131728f02773cb3b84e917bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867651"
---
# <span data-ttu-id="42141-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="42141-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="42141-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42141-102">SYNOPSIS</span></span>
<span data-ttu-id="42141-103">Usuwa mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42141-103">Removes an integration account map.</span></span>

## <span data-ttu-id="42141-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42141-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42141-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42141-105">DESCRIPTION</span></span>
<span data-ttu-id="42141-106">Polecenie cmdlet **Remove-AzIntegrationAccountMap** umożliwia usunięcie mapy konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42141-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="42141-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="42141-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="42141-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="42141-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="42141-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="42141-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="42141-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="42141-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="42141-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="42141-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="42141-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42141-112">EXAMPLES</span></span>

### <span data-ttu-id="42141-113">Przykład 1: usuwanie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="42141-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="42141-114">To polecenie powoduje usunięcie mapy kont integracji o nazwie IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="42141-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="42141-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42141-115">PARAMETERS</span></span>

### <span data-ttu-id="42141-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42141-116">-DefaultProfile</span></span>
<span data-ttu-id="42141-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="42141-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42141-118">-Force</span><span class="sxs-lookup"><span data-stu-id="42141-118">-Force</span></span>
<span data-ttu-id="42141-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42141-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42141-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="42141-120">-MapName</span></span>
<span data-ttu-id="42141-121">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42141-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42141-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42141-122">-Name</span></span>
<span data-ttu-id="42141-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42141-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="42141-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42141-124">-ResourceGroupName</span></span>
<span data-ttu-id="42141-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42141-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="42141-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42141-126">-Confirm</span></span>
<span data-ttu-id="42141-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42141-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42141-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42141-128">-WhatIf</span></span>
<span data-ttu-id="42141-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42141-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42141-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42141-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42141-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42141-131">CommonParameters</span></span>
<span data-ttu-id="42141-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42141-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42141-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42141-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42141-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42141-134">INPUTS</span></span>

### <span data-ttu-id="42141-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42141-135">System.String</span></span>

## <span data-ttu-id="42141-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42141-136">OUTPUTS</span></span>

### <span data-ttu-id="42141-137">System. void</span><span class="sxs-lookup"><span data-stu-id="42141-137">System.Void</span></span>

## <span data-ttu-id="42141-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42141-138">NOTES</span></span>

## <span data-ttu-id="42141-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42141-139">RELATED LINKS</span></span>

[<span data-ttu-id="42141-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="42141-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="42141-141">Nowe — AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="42141-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="42141-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="42141-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


