---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382403"
---
# New-AzApiManagementSslSetting

## STRESZCZENIe
Tworzy wystąpienie PsApiManagementSslSetting

## POLECENIA

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie pomocnika tworzenia wystąpienia PsApiManagementSslSetting.
To polecenie jest używane z poleceniem New-AzApiManagement.

## Przykłady

### Przykład 1: Tworzenie ustawienia SSL w celu włączenia protokołu TLS 1,0 zarówno w wewnętrznej bazie danych, jak i frontonie
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

Utwórz nowe wystąpienie PsApiManagementSslSetting, aby włączyć TLSv 1,0 zarówno na frontonie (między klientem a APIM), jak i zaplecza (między APIM i zapleczem) bramy ApiManagement.

## PARAMETRÓW

### -BackendProtocol
Ustawienia protokołu zabezpieczeń zaplecza. Ten parametr jest opcjonalny.
Prawidłowe ustawienia protokołu to `Tls11` tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
Ustawienia mechanizmów szyfrowania SSL w określonej kolejności. Ten parametr jest opcjonalny.
Prawidłowe ustawienia to `TripleDes168` Włączanie/wyłączanie wyjazdu Des 168

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -FrontendProtocol
Ustawienia protokołów zabezpieczeń frontonu. Ten parametr jest opcjonalny.
Prawidłowe ustawienia protokołu to `Tls11` tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
Ustawienia protokołu serwera, takie jak Http2. Ten parametr jest opcjonalny.
Prawidłowe ustawienia to `Http2` enable Http 2,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSslSettings

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzApiManagement](./New-AzApiManagement.md)

