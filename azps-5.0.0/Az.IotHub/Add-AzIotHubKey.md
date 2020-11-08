---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232248"
---
# <span data-ttu-id="d090e-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d090e-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="d090e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d090e-102">SYNOPSIS</span></span>
<span data-ttu-id="d090e-103">Tworzy klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="d090e-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="d090e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d090e-104">SYNTAX</span></span>

### <span data-ttu-id="d090e-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d090e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d090e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d090e-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d090e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d090e-107">DESCRIPTION</span></span>
<span data-ttu-id="d090e-108">Tworzy klucz dla podanej IotHub.</span><span class="sxs-lookup"><span data-stu-id="d090e-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="d090e-109">Nazwy tych, które nie są unikatowe, muszą być dobrze zarządzane.</span><span class="sxs-lookup"><span data-stu-id="d090e-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="d090e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d090e-110">EXAMPLES</span></span>

### <span data-ttu-id="d090e-111">Przykład 1 Dodawanie klucza do IotHub</span><span class="sxs-lookup"><span data-stu-id="d090e-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="d090e-112">Tworzy klucz o nazwie "MyKey" dla iothub "myiothub" z uprawnieniami RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="d090e-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="d090e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d090e-113">PARAMETERS</span></span>

### <span data-ttu-id="d090e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d090e-114">-DefaultProfile</span></span>
<span data-ttu-id="d090e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d090e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d090e-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="d090e-116">-HubId</span></span>
<span data-ttu-id="d090e-117">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d090e-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d090e-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="d090e-118">-KeyName</span></span>
<span data-ttu-id="d090e-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="d090e-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d090e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d090e-120">-Name</span></span>
<span data-ttu-id="d090e-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="d090e-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d090e-122">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="d090e-122">-PrimaryKey</span></span>
<span data-ttu-id="d090e-123">Klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="d090e-123">The primary key</span></span>

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

### <span data-ttu-id="d090e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d090e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d090e-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d090e-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d090e-126">-Prawa</span><span class="sxs-lookup"><span data-stu-id="d090e-126">-Rights</span></span>
<span data-ttu-id="d090e-127">Uprawnienia dla tego IOTHub</span><span class="sxs-lookup"><span data-stu-id="d090e-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="d090e-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d090e-128">-SecondaryKey</span></span>
<span data-ttu-id="d090e-129">Klucz pomocniczy</span><span class="sxs-lookup"><span data-stu-id="d090e-129">The Secondary Key</span></span>

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

### <span data-ttu-id="d090e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d090e-130">-Confirm</span></span>
<span data-ttu-id="d090e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d090e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d090e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d090e-132">-WhatIf</span></span>
<span data-ttu-id="d090e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d090e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d090e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d090e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d090e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d090e-135">CommonParameters</span></span>
<span data-ttu-id="d090e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d090e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d090e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d090e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d090e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d090e-138">INPUTS</span></span>

### <span data-ttu-id="d090e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d090e-139">System.String</span></span>

## <span data-ttu-id="d090e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d090e-140">OUTPUTS</span></span>

### <span data-ttu-id="d090e-141">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d090e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d090e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d090e-142">NOTES</span></span>

## <span data-ttu-id="d090e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d090e-143">RELATED LINKS</span></span>
