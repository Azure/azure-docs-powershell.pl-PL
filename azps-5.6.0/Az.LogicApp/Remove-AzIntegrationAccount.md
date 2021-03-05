---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962001"
---
# <span data-ttu-id="37665-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="37665-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="37665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37665-102">SYNOPSIS</span></span>
<span data-ttu-id="37665-103">Usuwa konto integracji.</span><span class="sxs-lookup"><span data-stu-id="37665-103">Removes an integration account.</span></span>

## <span data-ttu-id="37665-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37665-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37665-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="37665-105">DESCRIPTION</span></span>
<span data-ttu-id="37665-106">Polecenie **cmdlet Remove-AzIntegrationAccount** usuwa konto integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37665-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="37665-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37665-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="37665-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="37665-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="37665-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="37665-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="37665-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="37665-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="37665-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="37665-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="37665-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37665-112">EXAMPLES</span></span>

### <span data-ttu-id="37665-113">Przykład 1. Usuwanie konta integracji</span><span class="sxs-lookup"><span data-stu-id="37665-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="37665-114">To polecenie usuwa konto integracji o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="37665-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="37665-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37665-115">PARAMETERS</span></span>

### <span data-ttu-id="37665-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37665-116">-DefaultProfile</span></span>
<span data-ttu-id="37665-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="37665-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37665-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="37665-118">-Force</span></span>
<span data-ttu-id="37665-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37665-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37665-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37665-120">-Name</span></span>
<span data-ttu-id="37665-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37665-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="37665-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37665-122">-ResourceGroupName</span></span>
<span data-ttu-id="37665-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37665-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="37665-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37665-124">-Confirm</span></span>
<span data-ttu-id="37665-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37665-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37665-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37665-126">-WhatIf</span></span>
<span data-ttu-id="37665-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37665-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37665-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37665-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37665-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37665-129">CommonParameters</span></span>
<span data-ttu-id="37665-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37665-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37665-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37665-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37665-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37665-132">INPUTS</span></span>

### <span data-ttu-id="37665-133">System.String</span><span class="sxs-lookup"><span data-stu-id="37665-133">System.String</span></span>

## <span data-ttu-id="37665-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37665-134">OUTPUTS</span></span>

### <span data-ttu-id="37665-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="37665-135">System.Void</span></span>

## <span data-ttu-id="37665-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37665-136">NOTES</span></span>

## <span data-ttu-id="37665-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37665-137">RELATED LINKS</span></span>

[<span data-ttu-id="37665-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="37665-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="37665-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="37665-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="37665-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="37665-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


