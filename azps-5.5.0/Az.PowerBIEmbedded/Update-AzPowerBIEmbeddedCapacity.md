---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189347"
---
# <span data-ttu-id="daa4d-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="daa4d-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="daa4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa4d-102">SYNOPSIS</span></span>
<span data-ttu-id="daa4d-103">Modyfikuje wystąpienie osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="daa4d-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="daa4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="daa4d-104">SYNTAX</span></span>

### <span data-ttu-id="daa4d-105">ByNameAndResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="daa4d-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa4d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="daa4d-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daa4d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="daa4d-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa4d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="daa4d-108">DESCRIPTION</span></span>
<span data-ttu-id="daa4d-109">Polecenie Update-AzPowerBIEmbeddedCapacity cmdlet modyfikuje wystąpienie osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="daa4d-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="daa4d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="daa4d-110">EXAMPLES</span></span>

### <span data-ttu-id="daa4d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daa4d-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="daa4d-112">Modyfikuje wydajność o nazwie testcapacity w grupie testowej grupy zasobów, aby ustawić tagi jako klucz1:wartość1 i wartość2:wartość2 oraz dla administratora oraz podmiot testuser1@contoso.com testuser2@contoso.com zabezpieczeń usługi: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="daa4d-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="daa4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daa4d-113">PARAMETERS</span></span>

### <span data-ttu-id="daa4d-114">— Administrator</span><span class="sxs-lookup"><span data-stu-id="daa4d-114">-Administrator</span></span>
<span data-ttu-id="daa4d-115">Nazwy rozdzielone przecinkami, ustawiane jako administratorzy w zakresie pojemności.</span><span class="sxs-lookup"><span data-stu-id="daa4d-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="daa4d-116">W przypadku podmiotu zabezpieczeń usługi: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="daa4d-116">For service principal: <service principal object id>@<tenant id></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa4d-117">-DefaultProfile</span></span>
<span data-ttu-id="daa4d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="daa4d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daa4d-119">-InputObject</span></span>
<span data-ttu-id="daa4d-120">Obiekt wejściowy dla funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="daa4d-120">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="daa4d-121">-Name</span></span>
<span data-ttu-id="daa4d-122">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="daa4d-122">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="daa4d-123">-PassThru</span></span>
<span data-ttu-id="daa4d-124">Jeśli operacja zostanie pomyślnie ukończona, zostaną zwrócone szczegółowe informacje o usuniętej pojemności.</span><span class="sxs-lookup"><span data-stu-id="daa4d-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="daa4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="daa4d-126">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="daa4d-126">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa4d-127">-ResourceId</span></span>
<span data-ttu-id="daa4d-128">Osadzony zasób wydajności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="daa4d-128">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-129">- SKU</span><span class="sxs-lookup"><span data-stu-id="daa4d-129">-Sku</span></span>
<span data-ttu-id="daa4d-130">Nazwa sku dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="daa4d-130">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="daa4d-131">-Tag</span></span>
<span data-ttu-id="daa4d-132">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi dotyczące pojemności.</span><span class="sxs-lookup"><span data-stu-id="daa4d-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa4d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daa4d-133">-Confirm</span></span>
<span data-ttu-id="daa4d-134">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="daa4d-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="daa4d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa4d-135">-WhatIf</span></span>
<span data-ttu-id="daa4d-136">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="daa4d-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="daa4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa4d-137">CommonParameters</span></span>
<span data-ttu-id="daa4d-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa4d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa4d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa4d-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daa4d-140">INPUTS</span></span>

### <span data-ttu-id="daa4d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="daa4d-141">System.String</span></span>

### <span data-ttu-id="daa4d-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="daa4d-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="daa4d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="daa4d-143">OUTPUTS</span></span>

### <span data-ttu-id="daa4d-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="daa4d-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="daa4d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="daa4d-145">NOTES</span></span>

## <span data-ttu-id="daa4d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daa4d-146">RELATED LINKS</span></span>

[<span data-ttu-id="daa4d-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="daa4d-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="daa4d-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="daa4d-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
