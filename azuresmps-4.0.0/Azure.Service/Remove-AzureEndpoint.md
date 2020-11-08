---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055444"
---
# <span data-ttu-id="257c8-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="257c8-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="257c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="257c8-102">SYNOPSIS</span></span>
<span data-ttu-id="257c8-103">Usuwa punkt końcowy z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="257c8-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="257c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="257c8-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="257c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="257c8-105">DESCRIPTION</span></span>
<span data-ttu-id="257c8-106">Polecenie cmdlet **Remove-AzureEndpoint** usuwa punkt końcowy z obiektu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="257c8-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="257c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="257c8-107">EXAMPLES</span></span>

### <span data-ttu-id="257c8-108">Przykład 1: Usuwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="257c8-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="257c8-109">To polecenie pobiera konfigurację maszyny wirtualnej o nazwie VirtualMachine01 przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="257c8-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="257c8-110">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="257c8-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="257c8-111">To polecenie cmdlet umożliwia usunięcie punktu końcowego o nazwie http.</span><span class="sxs-lookup"><span data-stu-id="257c8-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="257c8-112">Polecenie przekazuje obiekt maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="257c8-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="257c8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="257c8-113">PARAMETERS</span></span>

### <span data-ttu-id="257c8-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="257c8-114">-InformationAction</span></span>
<span data-ttu-id="257c8-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="257c8-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="257c8-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="257c8-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="257c8-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="257c8-117">Continue</span></span>
- <span data-ttu-id="257c8-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="257c8-118">Ignore</span></span>
- <span data-ttu-id="257c8-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="257c8-119">Inquire</span></span>
- <span data-ttu-id="257c8-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="257c8-120">SilentlyContinue</span></span>
- <span data-ttu-id="257c8-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="257c8-121">Stop</span></span>
- <span data-ttu-id="257c8-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="257c8-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c8-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="257c8-123">-InformationVariable</span></span>
<span data-ttu-id="257c8-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="257c8-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="257c8-125">-Name</span></span>
<span data-ttu-id="257c8-126">Określa nazwę punktu końcowego, który zostanie usunięty przez to polecenie cmdlet z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="257c8-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c8-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="257c8-127">-Profile</span></span>
<span data-ttu-id="257c8-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="257c8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="257c8-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="257c8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="257c8-130">-VM</span></span>
<span data-ttu-id="257c8-131">Określa maszynę wirtualną, z której to polecenie cmdlet usuwa punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="257c8-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="257c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257c8-132">CommonParameters</span></span>
<span data-ttu-id="257c8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257c8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257c8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="257c8-135">INPUTS</span></span>

## <span data-ttu-id="257c8-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="257c8-136">OUTPUTS</span></span>

## <span data-ttu-id="257c8-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="257c8-137">NOTES</span></span>

## <span data-ttu-id="257c8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="257c8-138">RELATED LINKS</span></span>

[<span data-ttu-id="257c8-139">Dodaj-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="257c8-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="257c8-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="257c8-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="257c8-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="257c8-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="257c8-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="257c8-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="257c8-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="257c8-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


