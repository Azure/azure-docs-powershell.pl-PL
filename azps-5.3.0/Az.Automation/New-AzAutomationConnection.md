---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502325"
---
# <span data-ttu-id="2c687-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2c687-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="2c687-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c687-102">SYNOPSIS</span></span>
<span data-ttu-id="2c687-103">Umożliwia utworzenie połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2c687-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="2c687-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c687-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c687-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c687-105">DESCRIPTION</span></span>
<span data-ttu-id="2c687-106">Polecenie cmdlet **New-AzAutomationConnection** tworzy połączenie w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2c687-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="2c687-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c687-107">EXAMPLES</span></span>

### <span data-ttu-id="2c687-108">Przykład 1. Tworzenie połączenia dla ConnectionTypeName = Azure</span><span class="sxs-lookup"><span data-stu-id="2c687-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2c687-109">Pierwsze polecenie powoduje przypisanie tabeli skrótów wartości pól do zmiennej $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="2c687-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="2c687-110">Drugie polecenie tworzy połączenie platformy Azure o nazwie Connection12 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="2c687-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="2c687-111">W poleceniu są używane wartości pól połączenia w $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="2c687-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="2c687-112">Przykład 2: Tworzenie połączenia dla ConnectionTypeName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2c687-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2c687-113">Polecenie tworzy połączenie platformy Azure o nazwie Connection13 na koncie usługi Automation o nazwie AutomationAccount01 przy użyciu $RunAsAccountConnectionFieldValues i ConnectionTypeName = AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="2c687-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="2c687-114">Ta ConnectionTypeNamed = AzureServicePrincipal jest używana głównie dla konta usługi Azure Uruchom jako.</span><span class="sxs-lookup"><span data-stu-id="2c687-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="2c687-115">Przykład 3: Tworzenie połączenia dla ConnectionTypeName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="2c687-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2c687-116">Polecenie tworzy połączenie platformy Azure o nazwie Connection14 na koncie usługi Automation o nazwie AutomationAccount01 przy użyciu $ClassicRunAsAccountConnectionFieldValues i ConnectionTypeName = AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="2c687-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="2c687-117">Ta ConnectionTypeNamed = AzureClassicCertificate jest używana głównie dla klasycznego konta Uruchom jako w systemie Azure.</span><span class="sxs-lookup"><span data-stu-id="2c687-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="2c687-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c687-118">PARAMETERS</span></span>

### <span data-ttu-id="2c687-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c687-119">-AutomationAccountName</span></span>
<span data-ttu-id="2c687-120">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="2c687-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="2c687-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="2c687-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="2c687-122">Określa tabelę skrótów zawierającą pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="2c687-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="2c687-123">Klucze reprezentują pola połączeń dla określonego typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="2c687-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="2c687-124">Wartości reprezentują określone wartości każdego pola połączenia dla wystąpienia połączenia.</span><span class="sxs-lookup"><span data-stu-id="2c687-124">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c687-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="2c687-125">-ConnectionTypeName</span></span>
<span data-ttu-id="2c687-126">Określa nazwę typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="2c687-126">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c687-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c687-127">-DefaultProfile</span></span>
<span data-ttu-id="2c687-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2c687-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c687-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c687-129">-Description</span></span>
<span data-ttu-id="2c687-130">Określa opis połączenia.</span><span class="sxs-lookup"><span data-stu-id="2c687-130">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c687-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c687-131">-Name</span></span>
<span data-ttu-id="2c687-132">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="2c687-132">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c687-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c687-133">-ResourceGroupName</span></span>
<span data-ttu-id="2c687-134">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="2c687-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="2c687-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c687-135">CommonParameters</span></span>
<span data-ttu-id="2c687-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c687-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c687-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c687-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c687-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c687-138">INPUTS</span></span>

### <span data-ttu-id="2c687-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2c687-139">System.String</span></span>

### <span data-ttu-id="2c687-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="2c687-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="2c687-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c687-141">OUTPUTS</span></span>

### <span data-ttu-id="2c687-142">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="2c687-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="2c687-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c687-143">NOTES</span></span>

## <span data-ttu-id="2c687-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c687-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c687-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2c687-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="2c687-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2c687-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


