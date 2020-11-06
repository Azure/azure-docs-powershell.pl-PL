---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550988"
---
# <span data-ttu-id="216dd-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="216dd-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="216dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="216dd-102">SYNOPSIS</span></span>
<span data-ttu-id="216dd-103">Tworzy klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="216dd-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="216dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="216dd-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="216dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="216dd-105">DESCRIPTION</span></span>
<span data-ttu-id="216dd-106">Tworzy klucz dla podanej IotHub.</span><span class="sxs-lookup"><span data-stu-id="216dd-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="216dd-107">Nazwy tych, które nie są unikatowe, muszą być dobrze zarządzane.</span><span class="sxs-lookup"><span data-stu-id="216dd-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="216dd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="216dd-108">EXAMPLES</span></span>

### <span data-ttu-id="216dd-109">Przykład 1 Dodawanie klucza do IotHub</span><span class="sxs-lookup"><span data-stu-id="216dd-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="216dd-110">Tworzy klucz o nazwie "MyKey" dla iothub "myiothub" z uprawnieniami RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="216dd-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="216dd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="216dd-111">PARAMETERS</span></span>

### <span data-ttu-id="216dd-112">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="216dd-112">-KeyName</span></span>
<span data-ttu-id="216dd-113">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="216dd-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="216dd-114">-Name</span></span>
<span data-ttu-id="216dd-115">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="216dd-115">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-116">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="216dd-116">-PrimaryKey</span></span>
<span data-ttu-id="216dd-117">Klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="216dd-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="216dd-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="216dd-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-120">-Prawa</span><span class="sxs-lookup"><span data-stu-id="216dd-120">-Rights</span></span>
<span data-ttu-id="216dd-121">Uprawnienia dla tego IOTHub</span><span class="sxs-lookup"><span data-stu-id="216dd-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="216dd-122">-SecondaryKey</span></span>
<span data-ttu-id="216dd-123">Klucz pomocniczy</span><span class="sxs-lookup"><span data-stu-id="216dd-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216dd-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="216dd-124">-Confirm</span></span>
<span data-ttu-id="216dd-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="216dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216dd-126">-WhatIf</span></span>
<span data-ttu-id="216dd-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="216dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216dd-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="216dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216dd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216dd-129">-DefaultProfile</span></span>
<span data-ttu-id="216dd-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="216dd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="216dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216dd-131">CommonParameters</span></span>
<span data-ttu-id="216dd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="216dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216dd-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="216dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216dd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="216dd-134">INPUTS</span></span>

### <span data-ttu-id="216dd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="216dd-135">System.String</span></span>
<span data-ttu-id="216dd-136">Microsoft. Azure. Commands. Management. IotHub. models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="216dd-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="216dd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="216dd-137">OUTPUTS</span></span>

### <span data-ttu-id="216dd-138">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="216dd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="216dd-139">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="216dd-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="216dd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="216dd-140">NOTES</span></span>

## <span data-ttu-id="216dd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="216dd-141">RELATED LINKS</span></span>

