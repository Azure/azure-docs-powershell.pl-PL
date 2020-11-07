---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899028"
---
# <span data-ttu-id="1ed95-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1ed95-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="1ed95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ed95-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed95-103">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ed95-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ed95-104">SYNTAX</span></span>

### <span data-ttu-id="1ed95-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ed95-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed95-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ed95-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed95-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ed95-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed95-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ed95-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed95-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1ed95-109">DESCRIPTION</span></span>
<span data-ttu-id="1ed95-110">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ed95-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="1ed95-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ed95-111">EXAMPLES</span></span>

### <span data-ttu-id="1ed95-112">Przykład 1 — Usuwanie aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="1ed95-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="1ed95-113">Usuwa aplikację z identyfikatorem obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1ed95-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="1ed95-114">Przykład 2 — Usuwanie aplikacji według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ed95-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="1ed95-115">Usuwa aplikację z identyfikatorem aplikacji "f9c5ea4f-28f0-401A-a491-491a037fa346" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1ed95-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="1ed95-116">Przykład 3-usunięcie aplikacji przez potok rurociągowy</span><span class="sxs-lookup"><span data-stu-id="1ed95-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="1ed95-117">Pobiera aplikację o identyfikatorze obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzureRmADApplication w celu usunięcia aplikacji z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1ed95-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="1ed95-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ed95-118">PARAMETERS</span></span>

### <span data-ttu-id="1ed95-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ed95-119">-ApplicationId</span></span>
<span data-ttu-id="1ed95-120">Identyfikator aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1ed95-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed95-121">-DefaultProfile</span></span>
<span data-ttu-id="1ed95-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1ed95-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ed95-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ed95-123">-DisplayName</span></span>
<span data-ttu-id="1ed95-124">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ed95-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed95-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1ed95-125">-Force</span></span>
<span data-ttu-id="1ed95-126">Przełączanie w celu usunięcia aplikacji bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1ed95-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="1ed95-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ed95-127">-InputObject</span></span>
<span data-ttu-id="1ed95-128">Obiekt reprezentujący aplikację do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1ed95-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed95-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1ed95-129">-ObjectId</span></span>
<span data-ttu-id="1ed95-130">Identyfikator obiektu aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1ed95-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed95-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ed95-131">-PassThru</span></span>
<span data-ttu-id="1ed95-132">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="1ed95-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1ed95-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ed95-133">-Confirm</span></span>
<span data-ttu-id="1ed95-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed95-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed95-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed95-135">-WhatIf</span></span>
<span data-ttu-id="1ed95-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed95-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed95-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ed95-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed95-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed95-138">CommonParameters</span></span>
<span data-ttu-id="1ed95-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed95-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed95-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed95-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed95-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ed95-141">INPUTS</span></span>

### <span data-ttu-id="1ed95-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1ed95-142">System.Guid</span></span>

### <span data-ttu-id="1ed95-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1ed95-143">System.String</span></span>

### <span data-ttu-id="1ed95-144">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1ed95-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1ed95-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ed95-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1ed95-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ed95-146">OUTPUTS</span></span>

### <span data-ttu-id="1ed95-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ed95-147">System.Boolean</span></span>

## <span data-ttu-id="1ed95-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ed95-148">NOTES</span></span>
<span data-ttu-id="1ed95-149">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="1ed95-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1ed95-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ed95-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ed95-151">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1ed95-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="1ed95-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1ed95-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)



[<span data-ttu-id="1ed95-153">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1ed95-153">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

