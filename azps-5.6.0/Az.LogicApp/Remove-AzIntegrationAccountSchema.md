---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: b66c14eced87cb56b5e8b57766b268a63dbdb088
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961914"
---
# <span data-ttu-id="3fc3a-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3fc3a-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="3fc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc3a-103">Usuwa schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="3fc3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3fc3a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fc3a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3fc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc3a-106">Polecenie **cmdlet Remove-AzIntegrationAccountSchema** usuwa schemat konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="3fc3a-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="3fc3a-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3fc3a-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3fc3a-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3fc3a-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3fc3a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3fc3a-112">EXAMPLES</span></span>

### <span data-ttu-id="3fc3a-113">Przykład 1. Usuwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="3fc3a-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="3fc3a-114">To polecenie usuwa schemat konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="3fc3a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fc3a-115">PARAMETERS</span></span>

### <span data-ttu-id="3fc3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc3a-116">-DefaultProfile</span></span>
<span data-ttu-id="3fc3a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3fc3a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fc3a-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3fc3a-118">-Force</span></span>
<span data-ttu-id="3fc3a-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fc3a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3fc3a-120">-Name</span></span>
<span data-ttu-id="3fc3a-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3fc3a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc3a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3fc3a-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3fc3a-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3fc3a-124">-SchemaName</span></span>
<span data-ttu-id="3fc3a-125">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="3fc3a-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fc3a-126">-Confirm</span></span>
<span data-ttu-id="3fc3a-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fc3a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fc3a-128">-WhatIf</span></span>
<span data-ttu-id="3fc3a-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fc3a-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fc3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc3a-131">CommonParameters</span></span>
<span data-ttu-id="3fc3a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc3a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc3a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc3a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fc3a-134">INPUTS</span></span>

### <span data-ttu-id="3fc3a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3fc3a-135">System.String</span></span>

## <span data-ttu-id="3fc3a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fc3a-136">OUTPUTS</span></span>

### <span data-ttu-id="3fc3a-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="3fc3a-137">System.Void</span></span>

## <span data-ttu-id="3fc3a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3fc3a-138">NOTES</span></span>

## <span data-ttu-id="3fc3a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fc3a-139">RELATED LINKS</span></span>

[<span data-ttu-id="3fc3a-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3fc3a-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="3fc3a-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3fc3a-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="3fc3a-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3fc3a-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


