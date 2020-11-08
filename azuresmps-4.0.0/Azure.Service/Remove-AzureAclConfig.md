---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055141"
---
# <span data-ttu-id="ac9d4-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ac9d4-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="ac9d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9d4-103">Usuwa obiekt konfiguracji ACL z konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="ac9d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac9d4-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ac9d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9d4-106">Polecenie cmdlet **Remove-AzureAclConfig** usuwa obiekt konfiguracji listy kontroli dostępu (ACL) z konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="ac9d4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac9d4-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9d4-108">Przykład 1: Usuwanie konfiguracji ACL</span><span class="sxs-lookup"><span data-stu-id="ac9d4-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="ac9d4-109">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ac9d4-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ac9d4-110">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac9d4-111">To polecenie cmdlet usuwa konfigurację ACL punktu końcowego o nazwie sieć Web.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="ac9d4-112">Polecenie przekazanie wyniku do polecenia cmdlet **Update-AzureVM** , które powoduje zaktualizowanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="ac9d4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac9d4-113">PARAMETERS</span></span>

### <span data-ttu-id="ac9d4-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ac9d4-114">-EndpointName</span></span>
<span data-ttu-id="ac9d4-115">Określa nazwę punktu końcowego, z którego to polecenie cmdlet usuwa konfigurację ACL.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

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

### <span data-ttu-id="ac9d4-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ac9d4-116">-InformationAction</span></span>
<span data-ttu-id="ac9d4-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ac9d4-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ac9d4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac9d4-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ac9d4-119">Continue</span></span>
- <span data-ttu-id="ac9d4-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ac9d4-120">Ignore</span></span>
- <span data-ttu-id="ac9d4-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="ac9d4-121">Inquire</span></span>
- <span data-ttu-id="ac9d4-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ac9d4-122">SilentlyContinue</span></span>
- <span data-ttu-id="ac9d4-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-123">Stop</span></span>
- <span data-ttu-id="ac9d4-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ac9d4-124">Suspend</span></span>

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

### <span data-ttu-id="ac9d4-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ac9d4-125">-InformationVariable</span></span>
<span data-ttu-id="ac9d4-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ac9d4-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="ac9d4-127">-Profile</span></span>
<span data-ttu-id="ac9d4-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac9d4-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac9d4-130">-VM</span><span class="sxs-lookup"><span data-stu-id="ac9d4-130">-VM</span></span>
<span data-ttu-id="ac9d4-131">Określa maszynę wirtualną, z której to polecenie cmdlet usuwa konfigurację ACL.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="ac9d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9d4-132">CommonParameters</span></span>
<span data-ttu-id="ac9d4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9d4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9d4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9d4-135">INPUTS</span></span>

## <span data-ttu-id="ac9d4-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac9d4-136">OUTPUTS</span></span>

## <span data-ttu-id="ac9d4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac9d4-137">NOTES</span></span>

## <span data-ttu-id="ac9d4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac9d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac9d4-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ac9d4-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="ac9d4-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac9d4-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ac9d4-141">Nowe — AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ac9d4-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="ac9d4-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ac9d4-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="ac9d4-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac9d4-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


