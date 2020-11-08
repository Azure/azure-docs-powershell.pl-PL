---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055398"
---
# <span data-ttu-id="5bfc5-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="5bfc5-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="5bfc5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfc5-103">Modyfikuje obiekt konfiguracji ACL.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="5bfc5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bfc5-104">SYNTAX</span></span>

### <span data-ttu-id="5bfc5-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5bfc5-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5bfc5-107">Setrule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5bfc5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5bfc5-108">DESCRIPTION</span></span>
<span data-ttu-id="5bfc5-109">Polecenie cmdlet **Set-AzureAclConfig** modyfikuje obiekt konfiguracji listy kontroli dostępu (ACL) z istniejącej konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="5bfc5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bfc5-110">EXAMPLES</span></span>

### <span data-ttu-id="5bfc5-111">Przykład 1. Dodawanie reguły do nowej konfiguracji ACL</span><span class="sxs-lookup"><span data-stu-id="5bfc5-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="5bfc5-112">Pierwsze polecenie tworzy konfigurację listy ACL, a następnie zapisuje ją w zmiennej $Acl.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="5bfc5-113">Drugie polecenie doda nową regułę do konfiguracji przechowywanej w $Acl.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="5bfc5-114">Polecenie Określa akcję, podsieć, kolejność i opis reguły.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="5bfc5-115">Przykład 2: modyfikowanie reguły w konfiguracji ACL</span><span class="sxs-lookup"><span data-stu-id="5bfc5-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="5bfc5-116">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5bfc5-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="5bfc5-117">Polecenie przekazuje ten obiekt do polecenia cmdlet **Get-AzureAclConfig** za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5bfc5-118">To polecenie cmdlet pobiera konfigurację ACL dla punktu końcowego o nazwie sieć Web.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="5bfc5-119">Polecenie zapisuje ten obiekt konfiguracji ACL w zmiennej $Acl.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="5bfc5-120">Drugie polecenie modyfikuje regułę o IDENTYFIKATORze 0.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="5bfc5-121">Polecenie zmieni kolejność i opis reguły.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="5bfc5-122">Polecenie ostatnie ustawia obiekt konfiguracji ACL dla tej maszyny wirtualnej za pomocą polecenia cmdlet **Set-AzureEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="5bfc5-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="5bfc5-123">Polecenie powoduje również zaktualizowanie tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="5bfc5-124">Przykład 3: Usuwanie reguły z konfiguracji listy ACL</span><span class="sxs-lookup"><span data-stu-id="5bfc5-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="5bfc5-125">Pierwsze polecenie zapisuje obiekt konfiguracji ACL w zmiennej $Acl.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="5bfc5-126">Taki sam jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-126">This is the same as the previous example.</span></span>

<span data-ttu-id="5bfc5-127">Drugie polecenie usuwa regułę o IDENTYFIKATORze 0 z konfiguracji ACL w $Acl.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="5bfc5-128">Polecenie ostatnie ustawia obiekt konfiguracji ACL dla maszyny wirtualnej i aktualizuje tę maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="5bfc5-129">Taki sam jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="5bfc5-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bfc5-130">PARAMETERS</span></span>

### <span data-ttu-id="5bfc5-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="5bfc5-131">-ACL</span></span>
<span data-ttu-id="5bfc5-132">Określa obiekt konfiguracji ACL, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-133">-Action</span><span class="sxs-lookup"><span data-stu-id="5bfc5-133">-Action</span></span>
<span data-ttu-id="5bfc5-134">Określa akcję reguły, którą to polecenie cmdlet dodaje lub modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="5bfc5-135">Prawidłowe wartości to: Permit i Deny.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-136">-AddRule</span></span>
<span data-ttu-id="5bfc5-137">Wskazuje, że to polecenie cmdlet dodaje regułę do konfiguracji ACL.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-138">— Opis</span><span class="sxs-lookup"><span data-stu-id="5bfc5-138">-Description</span></span>
<span data-ttu-id="5bfc5-139">Określa opis reguły, którą to polecenie cmdlet dodaje lub modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5bfc5-140">-InformationAction</span></span>
<span data-ttu-id="5bfc5-141">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5bfc5-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5bfc5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bfc5-143">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5bfc5-143">Continue</span></span>
- <span data-ttu-id="5bfc5-144">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5bfc5-144">Ignore</span></span>
- <span data-ttu-id="5bfc5-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="5bfc5-145">Inquire</span></span>
- <span data-ttu-id="5bfc5-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5bfc5-146">SilentlyContinue</span></span>
- <span data-ttu-id="5bfc5-147">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5bfc5-147">Stop</span></span>
- <span data-ttu-id="5bfc5-148">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5bfc5-148">Suspend</span></span>

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

### <span data-ttu-id="5bfc5-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5bfc5-149">-InformationVariable</span></span>
<span data-ttu-id="5bfc5-150">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5bfc5-151">-Order (kolejność)</span><span class="sxs-lookup"><span data-stu-id="5bfc5-151">-Order</span></span>
<span data-ttu-id="5bfc5-152">Określa kolejność przetwarzania dla reguły, którą to polecenie cmdlet dodaje lub modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="5bfc5-153">-RemoteSubnet</span></span>
<span data-ttu-id="5bfc5-154">Określa podsieć zdalną dla reguły, którą to polecenie cmdlet dodaje lub modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="5bfc5-155">Określa adres w formacie CIDR (Classless międzydomain Routing).</span><span class="sxs-lookup"><span data-stu-id="5bfc5-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-156">-RemoveRule</span></span>
<span data-ttu-id="5bfc5-157">Wskazuje, że to polecenie cmdlet usuwa regułę z konfiguracji ACL.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="5bfc5-158">-RuleId</span></span>
<span data-ttu-id="5bfc5-159">Określa identyfikator reguły, która jest usuwana lub modyfikowana przez to polecenie cmdlet dla konfiguracji ACL.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-160">-Setrule</span><span class="sxs-lookup"><span data-stu-id="5bfc5-160">-SetRule</span></span>
<span data-ttu-id="5bfc5-161">Wskazuje, że to polecenie cmdlet modyfikuje regułę w konfiguracji ACL.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfc5-162">CommonParameters</span></span>
<span data-ttu-id="5bfc5-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfc5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfc5-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bfc5-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfc5-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bfc5-165">INPUTS</span></span>

## <span data-ttu-id="5bfc5-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bfc5-166">OUTPUTS</span></span>

## <span data-ttu-id="5bfc5-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bfc5-167">NOTES</span></span>

## <span data-ttu-id="5bfc5-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bfc5-168">RELATED LINKS</span></span>

[<span data-ttu-id="5bfc5-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="5bfc5-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="5bfc5-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5bfc5-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="5bfc5-171">Nowe — AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="5bfc5-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="5bfc5-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="5bfc5-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="5bfc5-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bfc5-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="5bfc5-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5bfc5-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


