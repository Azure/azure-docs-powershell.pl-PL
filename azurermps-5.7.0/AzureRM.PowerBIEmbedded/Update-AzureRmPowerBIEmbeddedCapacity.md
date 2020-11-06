---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525042"
---
# <span data-ttu-id="15a0c-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="15a0c-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="15a0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="15a0c-103">Umożliwia zmodyfikowanie wystąpienia osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="15a0c-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15a0c-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="15a0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="15a0c-106">Polecenie cmdlet Update-AzureRmPowerBIEmbeddedCapacity powoduje zmodyfikowanie wystąpienia osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="15a0c-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="15a0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15a0c-107">EXAMPLES</span></span>

### <span data-ttu-id="15a0c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15a0c-108">Example 1</span></span>
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

<span data-ttu-id="15a0c-109">Modyfikuje pojemność o nazwie testcapacity w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="15a0c-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="15a0c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15a0c-110">PARAMETERS</span></span>

### <span data-ttu-id="15a0c-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15a0c-111">-Name</span></span>
<span data-ttu-id="15a0c-112">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="15a0c-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a0c-113">-ResourceGroupName</span></span>
<span data-ttu-id="15a0c-114">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="15a0c-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="15a0c-115">-Sku</span></span>
<span data-ttu-id="15a0c-116">Nazwa jednostki SKU dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="15a0c-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="15a0c-117">-Tag</span></span>
<span data-ttu-id="15a0c-118">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.</span><span class="sxs-lookup"><span data-stu-id="15a0c-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="15a0c-119">-Administrator</span><span class="sxs-lookup"><span data-stu-id="15a0c-119">-Administrator</span></span>
<span data-ttu-id="15a0c-120">Nazwy pojemności rozdzielone przecinkami, które są ustawiane jako administrator na stanowisku</span><span class="sxs-lookup"><span data-stu-id="15a0c-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a0c-121">-ResourceId</span></span>
<span data-ttu-id="15a0c-122">Identyfikator zasobu osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="15a0c-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15a0c-123">-InputObject</span></span>
<span data-ttu-id="15a0c-124">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="15a0c-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15a0c-125">-PassThru</span></span>
<span data-ttu-id="15a0c-126">Zwraca szczegóły usuniętej pojemności, jeśli operacja zostanie ukończona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="15a0c-126">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="15a0c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15a0c-127">-Confirm</span></span>
<span data-ttu-id="15a0c-128">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="15a0c-128">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="15a0c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a0c-129">-WhatIf</span></span>
<span data-ttu-id="15a0c-130">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="15a0c-130">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="15a0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a0c-131">CommonParameters</span></span>
<span data-ttu-id="15a0c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a0c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a0c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a0c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15a0c-134">INPUTS</span></span>

### <span data-ttu-id="15a0c-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="15a0c-135">None</span></span>
<span data-ttu-id="15a0c-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="15a0c-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15a0c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15a0c-137">OUTPUTS</span></span>

### <span data-ttu-id="15a0c-138">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="15a0c-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="15a0c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15a0c-139">NOTES</span></span>

## <span data-ttu-id="15a0c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15a0c-140">RELATED LINKS</span></span>

[<span data-ttu-id="15a0c-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="15a0c-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="15a0c-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="15a0c-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
