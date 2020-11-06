---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545240"
---
# <span data-ttu-id="6d9b2-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="6d9b2-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="6d9b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9b2-103">Tworzy klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d9b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d9b2-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9b2-106">Tworzy klucz dla podanej IotHub.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="6d9b2-107">Nazwy tych, które nie są unikatowe, muszą być dobrze zarządzane.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="6d9b2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d9b2-108">EXAMPLES</span></span>

### <span data-ttu-id="6d9b2-109">Przykład 1 Dodawanie klucza do IotHub</span><span class="sxs-lookup"><span data-stu-id="6d9b2-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="6d9b2-110">Tworzy klucz o nazwie "MyKey" dla iothub "myiothub" z uprawnieniami RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="6d9b2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d9b2-111">PARAMETERS</span></span>

### <span data-ttu-id="6d9b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9b2-112">-DefaultProfile</span></span>
<span data-ttu-id="6d9b2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d9b2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d9b2-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="6d9b2-114">-KeyName</span></span>
<span data-ttu-id="6d9b2-115">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="6d9b2-115">Name of the Key</span></span>

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

### <span data-ttu-id="6d9b2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d9b2-116">-Name</span></span>
<span data-ttu-id="6d9b2-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="6d9b2-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="6d9b2-118">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="6d9b2-118">-PrimaryKey</span></span>
<span data-ttu-id="6d9b2-119">Klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="6d9b2-119">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="6d9b2-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6d9b2-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6d9b2-122">-Prawa</span><span class="sxs-lookup"><span data-stu-id="6d9b2-122">-Rights</span></span>
<span data-ttu-id="6d9b2-123">Uprawnienia dla tego IOTHub</span><span class="sxs-lookup"><span data-stu-id="6d9b2-123">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9b2-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="6d9b2-124">-SecondaryKey</span></span>
<span data-ttu-id="6d9b2-125">Klucz pomocniczy</span><span class="sxs-lookup"><span data-stu-id="6d9b2-125">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9b2-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d9b2-126">-Confirm</span></span>
<span data-ttu-id="6d9b2-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9b2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9b2-128">-WhatIf</span></span>
<span data-ttu-id="6d9b2-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9b2-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9b2-131">CommonParameters</span></span>
<span data-ttu-id="6d9b2-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9b2-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9b2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9b2-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9b2-134">INPUTS</span></span>

### <span data-ttu-id="6d9b2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6d9b2-135">System.String</span></span>

## <span data-ttu-id="6d9b2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d9b2-136">OUTPUTS</span></span>

### <span data-ttu-id="6d9b2-137">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d9b2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="6d9b2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d9b2-138">NOTES</span></span>

## <span data-ttu-id="6d9b2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d9b2-139">RELATED LINKS</span></span>
