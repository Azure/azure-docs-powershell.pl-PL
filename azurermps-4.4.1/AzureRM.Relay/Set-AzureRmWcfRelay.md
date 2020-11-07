---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716669"
---
# <span data-ttu-id="9b21f-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="9b21f-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="9b21f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b21f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b21f-103">Umożliwia zaktualizowanie opisu WcfRelay w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="9b21f-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b21f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b21f-104">SYNTAX</span></span>

### <span data-ttu-id="9b21f-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9b21f-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b21f-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="9b21f-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b21f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b21f-107">DESCRIPTION</span></span>
<span data-ttu-id="9b21f-108">Polecenie cmdlet Set-AzureRmWcfRelay aktualizuje opis WcfRelay w określonej przestrzeni nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="9b21f-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="9b21f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b21f-109">EXAMPLES</span></span>

### <span data-ttu-id="9b21f-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b21f-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="9b21f-111">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="9b21f-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="9b21f-112">Umożliwia zaktualizowanie określonego WcfRelay przy użyciu nowego opisu w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="9b21f-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="9b21f-113">W tym przykładzie zostanie zaktualizowana właściwość UserMetadata o nową wartość.</span><span class="sxs-lookup"><span data-stu-id="9b21f-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="9b21f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b21f-114">PARAMETERS</span></span>

### <span data-ttu-id="9b21f-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="9b21f-115">-UserMetadata</span></span>
<span data-ttu-id="9b21f-116">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9b21f-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b21f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b21f-117">-Confirm</span></span>
<span data-ttu-id="9b21f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b21f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b21f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b21f-119">-WhatIf</span></span>
<span data-ttu-id="9b21f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b21f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b21f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b21f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b21f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b21f-122">-InputObject</span></span>
<span data-ttu-id="9b21f-123">Obiekt WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="9b21f-123">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b21f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b21f-124">-Name</span></span>
<span data-ttu-id="9b21f-125">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="9b21f-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9b21f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b21f-126">-Namespace</span></span>
<span data-ttu-id="9b21f-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9b21f-127">Namespace Name.</span></span>

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

### <span data-ttu-id="9b21f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b21f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b21f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b21f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b21f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b21f-130">-DefaultProfile</span></span>
<span data-ttu-id="9b21f-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b21f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b21f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b21f-132">CommonParameters</span></span>
<span data-ttu-id="9b21f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b21f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b21f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b21f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b21f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b21f-135">INPUTS</span></span>

### <span data-ttu-id="9b21f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b21f-136">-ResourceGroupName</span></span>
<span data-ttu-id="9b21f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9b21f-137">System.String</span></span>

### <span data-ttu-id="9b21f-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9b21f-138">-NamespaceName</span></span>
<span data-ttu-id="9b21f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9b21f-139">System.String</span></span>

### <span data-ttu-id="9b21f-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="9b21f-140">-WcfRelayName</span></span>
<span data-ttu-id="9b21f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b21f-141">System.String</span></span>

### <span data-ttu-id="9b21f-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b21f-142">-InputObject</span></span>
<span data-ttu-id="9b21f-143">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="9b21f-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="9b21f-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="9b21f-144">-WcfRelayType</span></span>
<span data-ttu-id="9b21f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9b21f-145">System.String</span></span>

### <span data-ttu-id="9b21f-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="9b21f-146">-UserMetadata</span></span>
<span data-ttu-id="9b21f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9b21f-147">System.String</span></span>

## <span data-ttu-id="9b21f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b21f-148">OUTPUTS</span></span>

### <span data-ttu-id="9b21f-149">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="9b21f-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="9b21f-150">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b21f-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="9b21f-151">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="9b21f-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="9b21f-152">Relaytype: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: prawda IsDynamic: FAŁSZ UserMetadata: UserMetadata to symbol zastępczy umożliwiający przechowywanie danych ciągów zdefiniowanych przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisu riptive, takich jak lista zespołów i informacje kontaktowe, także w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9b21f-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="9b21f-153">Identyfikator:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel dni/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="9b21f-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="9b21f-154">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="9b21f-154">Example 2 - Properties</span></span>

### <span data-ttu-id="9b21f-155">Microsoft. Azure. Commands. Relay. modele. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="9b21f-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="9b21f-156">Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: prawda RequiresTransportSecurity: prawda IsDynamic: false UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel dni/obszary nazw/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="9b21f-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="9b21f-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b21f-157">NOTES</span></span>

## <span data-ttu-id="9b21f-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b21f-158">RELATED LINKS</span></span>

