---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185163"
---
# <span data-ttu-id="9151b-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9151b-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="9151b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9151b-102">SYNOPSIS</span></span>
<span data-ttu-id="9151b-103">Usuwa mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9151b-103">Removes an integration account map.</span></span>

## <span data-ttu-id="9151b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9151b-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9151b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9151b-105">DESCRIPTION</span></span>
<span data-ttu-id="9151b-106">Polecenie **cmdlet Remove-AzIntegrationAccountMap** usuwa mapę konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9151b-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="9151b-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="9151b-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="9151b-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="9151b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9151b-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9151b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9151b-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="9151b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9151b-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="9151b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9151b-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9151b-112">EXAMPLES</span></span>

### <span data-ttu-id="9151b-113">Przykład 1. Usuwanie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="9151b-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="9151b-114">To polecenie usuwa mapę konta integracji o nazwie IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="9151b-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="9151b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9151b-115">PARAMETERS</span></span>

### <span data-ttu-id="9151b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9151b-116">-DefaultProfile</span></span>
<span data-ttu-id="9151b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9151b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9151b-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9151b-118">-Force</span></span>
<span data-ttu-id="9151b-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9151b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9151b-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="9151b-120">-MapName</span></span>
<span data-ttu-id="9151b-121">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9151b-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="9151b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9151b-122">-Name</span></span>
<span data-ttu-id="9151b-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9151b-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9151b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9151b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9151b-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9151b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9151b-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9151b-126">-Confirm</span></span>
<span data-ttu-id="9151b-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9151b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9151b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9151b-128">-WhatIf</span></span>
<span data-ttu-id="9151b-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9151b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9151b-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9151b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9151b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9151b-131">CommonParameters</span></span>
<span data-ttu-id="9151b-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9151b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9151b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9151b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9151b-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9151b-134">INPUTS</span></span>

### <span data-ttu-id="9151b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9151b-135">System.String</span></span>

## <span data-ttu-id="9151b-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9151b-136">OUTPUTS</span></span>

### <span data-ttu-id="9151b-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="9151b-137">System.Void</span></span>

## <span data-ttu-id="9151b-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9151b-138">NOTES</span></span>

## <span data-ttu-id="9151b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9151b-139">RELATED LINKS</span></span>

[<span data-ttu-id="9151b-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9151b-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="9151b-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9151b-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="9151b-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9151b-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


