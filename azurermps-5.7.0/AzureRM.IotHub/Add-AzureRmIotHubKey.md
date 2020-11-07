---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: c56b147c5ac62e376eff1159eb679c5a692eb1b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548112"
---
# <span data-ttu-id="7452d-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7452d-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="7452d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7452d-102">SYNOPSIS</span></span>
<span data-ttu-id="7452d-103">Tworzy klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="7452d-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7452d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7452d-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7452d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7452d-105">DESCRIPTION</span></span>
<span data-ttu-id="7452d-106">Tworzy klucz dla podanej IotHub.</span><span class="sxs-lookup"><span data-stu-id="7452d-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="7452d-107">Nazwy tych, które nie są unikatowe, muszą być dobrze zarządzane.</span><span class="sxs-lookup"><span data-stu-id="7452d-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="7452d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7452d-108">EXAMPLES</span></span>

### <span data-ttu-id="7452d-109">Przykład 1 Dodawanie klucza do IotHub</span><span class="sxs-lookup"><span data-stu-id="7452d-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="7452d-110">Tworzy klucz o nazwie "MyKey" dla iothub "myiothub" z uprawnieniami RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="7452d-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="7452d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7452d-111">PARAMETERS</span></span>

### <span data-ttu-id="7452d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7452d-112">-DefaultProfile</span></span>
<span data-ttu-id="7452d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7452d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="7452d-114">-KeyName</span></span>
<span data-ttu-id="7452d-115">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="7452d-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7452d-116">-Name</span></span>
<span data-ttu-id="7452d-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="7452d-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-118">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="7452d-118">-PrimaryKey</span></span>
<span data-ttu-id="7452d-119">Klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="7452d-119">The primary key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7452d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7452d-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7452d-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-122">-Prawa</span><span class="sxs-lookup"><span data-stu-id="7452d-122">-Rights</span></span>
<span data-ttu-id="7452d-123">Uprawnienia dla tego IOTHub</span><span class="sxs-lookup"><span data-stu-id="7452d-123">The permissions for this IOTHub</span></span>

```yaml
Type: PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7452d-124">-SecondaryKey</span></span>
<span data-ttu-id="7452d-125">Klucz pomocniczy</span><span class="sxs-lookup"><span data-stu-id="7452d-125">The Secondary Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7452d-126">-Confirm</span></span>
<span data-ttu-id="7452d-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7452d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7452d-128">-WhatIf</span></span>
<span data-ttu-id="7452d-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7452d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7452d-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7452d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7452d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7452d-131">CommonParameters</span></span>
<span data-ttu-id="7452d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7452d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7452d-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7452d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7452d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7452d-134">INPUTS</span></span>

### <span data-ttu-id="7452d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7452d-135">System.String</span></span>
<span data-ttu-id="7452d-136">Microsoft. Azure. Commands. Management. IotHub. models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="7452d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="7452d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7452d-137">OUTPUTS</span></span>

### <span data-ttu-id="7452d-138">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7452d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="7452d-139">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. MODELES. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="7452d-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="7452d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7452d-140">NOTES</span></span>

## <span data-ttu-id="7452d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7452d-141">RELATED LINKS</span></span>
