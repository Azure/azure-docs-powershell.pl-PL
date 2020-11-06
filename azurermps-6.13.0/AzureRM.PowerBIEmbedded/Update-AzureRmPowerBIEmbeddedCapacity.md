---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552612"
---
# <span data-ttu-id="262e9-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="262e9-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="262e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="262e9-102">SYNOPSIS</span></span>
<span data-ttu-id="262e9-103">Umożliwia zmodyfikowanie wystąpienia osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="262e9-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="262e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="262e9-104">SYNTAX</span></span>

### <span data-ttu-id="262e9-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="262e9-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="262e9-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="262e9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="262e9-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="262e9-108">DESCRIPTION</span></span>
<span data-ttu-id="262e9-109">Polecenie cmdlet Update-AzureRmPowerBIEmbeddedCapacity powoduje zmodyfikowanie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="262e9-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="262e9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="262e9-110">EXAMPLES</span></span>

### <span data-ttu-id="262e9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="262e9-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="262e9-112">Modyfikuje pojemność o nazwie testcapacity w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="262e9-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="262e9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="262e9-113">PARAMETERS</span></span>

### <span data-ttu-id="262e9-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="262e9-114">-Administrator</span></span>
<span data-ttu-id="262e9-115">Nazwy pojemności rozdzielone przecinkami, które są ustawiane jako administrator na stanowisku</span><span class="sxs-lookup"><span data-stu-id="262e9-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="262e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262e9-116">-DefaultProfile</span></span>
<span data-ttu-id="262e9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="262e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262e9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="262e9-118">-InputObject</span></span>
<span data-ttu-id="262e9-119">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="262e9-119">Input object for Piping</span></span>

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

### <span data-ttu-id="262e9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="262e9-120">-Name</span></span>
<span data-ttu-id="262e9-121">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="262e9-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="262e9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="262e9-122">-PassThru</span></span>
<span data-ttu-id="262e9-123">Zwraca szczegóły usuniętej pojemności, jeśli operacja zostanie ukończona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="262e9-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="262e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="262e9-125">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="262e9-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="262e9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="262e9-126">-ResourceId</span></span>
<span data-ttu-id="262e9-127">Identyfikator zasobu osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="262e9-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="262e9-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="262e9-128">-Sku</span></span>
<span data-ttu-id="262e9-129">Nazwa jednostki SKU dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="262e9-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="262e9-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="262e9-130">-Tag</span></span>
<span data-ttu-id="262e9-131">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.</span><span class="sxs-lookup"><span data-stu-id="262e9-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="262e9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="262e9-132">-Confirm</span></span>
<span data-ttu-id="262e9-133">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="262e9-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="262e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262e9-134">-WhatIf</span></span>
<span data-ttu-id="262e9-135">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="262e9-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="262e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262e9-136">CommonParameters</span></span>
<span data-ttu-id="262e9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262e9-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262e9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262e9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262e9-139">INPUTS</span></span>

### <span data-ttu-id="262e9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="262e9-140">System.String</span></span>

### <span data-ttu-id="262e9-141">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="262e9-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="262e9-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="262e9-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="262e9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="262e9-143">OUTPUTS</span></span>

### <span data-ttu-id="262e9-144">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="262e9-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="262e9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="262e9-145">NOTES</span></span>

## <span data-ttu-id="262e9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="262e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="262e9-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="262e9-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="262e9-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="262e9-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
